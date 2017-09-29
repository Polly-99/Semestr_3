#include <iostream>

template <typename T>
class TVector
{
    T * ptr;
    size_t size;
    size_t capacity;
public:
    TVector()
            :ptr(nullptr)
            ,size(0)
            ,capacity(0)
    {}

    TVector (const TVector & rhs)
            :size(rhs.size)
            , capacity(rhs.capacity)
    {
            ptr = new T[capacity];
            for (int i = 0; i < size; i++)
            {
                ptr[i] = rhs.ptr[i];
            }
    }

    TVector (TVector && rhs)
    :size(rhs.size)
    , capacity (rhs.capacity)
    {
        std::swap(ptr, rhs.ptr);
        rhs.size = 0;
        rhs.capacity = 0;
    }

    TVector& operator=(const TVector& rhs)
    {
        if (this == &rhs)
            return *this;
        size = rhs.size;
        capacity = rhs.capacity;
        delete[] ptr;
        ptr = new T[capacity];
        for (int i = 0; i < size; i++)
        {
           ptr[i] = rhs.ptr[i];
        }
        return *this;
    }

    TVector& operator=(TVector&& rhs)
    {
        if (this == &rhs)
            return *this;
        size = rhs.size;
        capacity = rhs.capacity;
        std::swap(ptr, rhs.ptr);
        delete [] rhs.ptr;
        rhs.size = 0;
        rhs.capacity = 0;
        return *this;
    }

    ~TVector()
    {
        if (ptr != nullptr)
            delete[] ptr;
        size=0;
        capacity = 0;
    }

};
