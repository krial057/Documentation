.. _renvector4.rst:

***********************
Vector4 class reference
***********************

.. namespace:: RN
.. class:: Vector4

+---------------------+--------------------------------------+
|   **Availability**  |              Rayne 1.0               |
+---------------------+--------------------------------------+
| **Declared in**     | RNVector.h                           |
+---------------------+--------------------------------------+

Overview
========

.. inheritance_diagram::

The Vector4 class provides a 4d floating point vector implementation. On systems with SIMD support,
Vector4 is aligned to 16 byte boundaries and uses optimized SSE/NEON code. Vector4 is trivially copyable.

Tasks
=====

Construction
------------

* :cpp:func:`Vector4() <Vector4::Vector4>`
* :cpp:func:`Vector4(float n) <Vector4::Vector4>`
* :cpp:func:`Vector4(float x, float y, float z, float w) <Vector4::Vector4>`
* :cpp:func:`Vector4(const Vector4& other) explicit <Vector4::Vector4>`
* :cpp:func:`Vector4(const Vector3& other, float w = 0.0f) explicit <Vector4::Vector4>`
* :cpp:func:`Vector4(const Vector2& other, float z = 0.0f, float w = 0.0f) explicit <Vector4::Vector4>`
  
Comparison
----------

* :cpp:func:`operator== (const Vector4& other) const <Vector4::operator==>`
* :cpp:func:`operator!= (const Vector4& other) const <Vector4::operator!=>`
* :cpp:func:`IsEqual(const Vector4& other, float epsilon) const <Vector4::IsEqual>`

Unary operators
---------------

* :cpp:func:`operator- () const <Vector4::operator->`
  
Binary operators
----------------

* :cpp:func:`operator+ (const Vector4& other) const <Vector4::operator+>`
* :cpp:func:`operator- (const Vector4& other) const <Vector4::operator->`
* :cpp:func:`operator* (const Vector4& other) const <Vector4::operator*>`
* :cpp:func:`operator/ (const Vector4& other) const <Vector4::operator/>`
* :cpp:func:`operator* (const float n) const <Vector4::operator*>`
* :cpp:func:`operator/ (const float n) const <Vector4::operator/>`
* :cpp:func:`operator+= (const Vector4& other) <Vector4::operator+=>`
* :cpp:func:`operator-= (const Vector4& other) <Vector4::operator-=>`
* :cpp:func:`operator*= (const Vector4& other) <Vector4::operator*=>`
* :cpp:func:`operator/= (const Vector4& other) <Vector4::operator/=>`

Accessors
---------

* :cpp:func:`Length() const <Vector4::Length>`
* :cpp:func:`Dot(const Vector4& other) const <Vector4::Dot>`
* :cpp:func:`Cross(const Vector4& other) const <Vector4::Cross>`

 
Mutation
--------

* :cpp:func:`Normalize(float n) <Vector4::Normalize>`
  
Instance Methods
================

.. class:: Vector4 

	.. function:: Vector4()

		Initializes the `x`, `y`, `z` and `w` component to `0.0f`

	.. function:: Vector4(float n)

		Initializes the `x`, `y`, `z` and `w` component to the value in `n`

	.. function:: Vector4(float x, float y, float z, float w)

		Initialized the `x`, `y`, `z` and `w` component to the `x`, `y`, `z` and `w` parameters respectively

	.. function:: Vector4(const Vector2& other, float z = 0.0f, float w = 0.0f)

		Initialized the `x` and `y` component to the `x`, and `y` components of the `other` vector and the `z` and `w` components to the `z` and `w` components respectively

	.. function:: Vector4(const Vector3& other, float w = 0.0f)

		Initialized the `x` and `y` component to the `x`, and `y` components of the `other` vector and the `z` and `w` components to the `z` and `w` components respectively

	.. function:: Vector4(const Vector4& other)

		Initialized the `x`, `y`, `z` and `w` component to the `x`, `y`, `z` and `w` components of the `other` vector

	.. function:: bool operator== (const Vector4& other) const

		Compares the vector against the other and returns `true` if they are deemed equal.
		This function is equivalent to calling `IsEqual(other, k::EpsilonFloat)`

	.. function:: bool operator!= (const Vector4& other) const

		Compares the vector against the other and returns `true` if they are deemed unequal.
		This function is equivalent to calling `!IsEqual(other, k::EpsilonFloat)`

	.. function:: bool IsEqual(const Vector4& other, float epsilon) const

		Compares the vector against the other using the provided epsilon. The function will subtract
		each component of the respective component of the other vector and compares them against the delta.
		If one exceeds the delta, the two vectors are deemed unequal and the function returns false.

	.. function:: Vector4 operator- () const

		Returns a new vector with its components negated.

	.. function:: Vector4 operator+ (const Vector4& other) const

		Returns a new vector with all components of the `other` vector added to the components of `this`

	.. function:: Vector4 operator- (const Vector4& other) const

		Returns a new vector with all components of the `other` vector subtracted from the components of `this`

	.. function:: Vector4 operator* (const Vector4& other) const

		Returns a new vector with all components of `this` multiplied with the components of the `other` vector

	.. function:: Vector4 operator/ (const Vector4& other) const

		Returns a new vector with all components of `this` divided by the components of the `other` vector

	.. function:: Vector4 operator* (const float n) const

		Returns a new vector with all components of `this` multiplied with `n`

	.. function:: Vector4 operator/ (const float n) const

		Returns a new vector with all components of `this` divided by `n`

	.. function:: Vector4& operator+= (const Vector4& other)

		Adds the components of the `other` vector to the respective components of the vector

		:return: Reference to the mutated vector

	.. function:: Vector4& operator-= (const Vector4& other)

		Subtracts the components of the `other` vector from the respective components of the vector

		:return: Reference to the mutated vector

	.. function:: Vector4& operator*= (const Vector4& other)

		Multiplies the components of the `other` vector with the respective components of the vector

		:return: Reference to the mutated vector

	.. function:: Vector4& operator/= (const Vector4& other)

		Divides the components of the `other` vector by the respective components of the vector

		:return: Reference to the mutated vector

	.. function:: float Length() const

		Returns the length of the vector

	.. function:: float Dot(const Vector4& other) const

		Returns the dot product of the vector and the `other` vector

	.. function:: Vector4 Cross(const Vector4& other) const

		Returns the cross product of the vector and the `other` vector

	.. function:: Vector4& Normalize(const float n)

		Normalizes the vector to the constant `n`

		:return: Reference to the mutated vector

Member
======

.. class:: Vector4

	.. member:: float x

		The x component of the vector

	.. member:: float y

		The y component of the vector

	.. member:: float z

		The z component of the vector

	.. member:: float w

		The w component of the vector
