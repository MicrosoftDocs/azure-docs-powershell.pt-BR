---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: be6c9ee6c0db12e324786052348209703b79601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427040"
---
# <span data-ttu-id="7e32e-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7e32e-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="7e32e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e32e-102">SYNOPSIS</span></span>
<span data-ttu-id="7e32e-103">Obtém um ou mais usuários.</span><span class="sxs-lookup"><span data-stu-id="7e32e-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e32e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e32e-104">SYNTAX</span></span>

### <span data-ttu-id="7e32e-105">Obter todos os usuários (padrão)</span><span class="sxs-lookup"><span data-stu-id="7e32e-105">Get all users (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e32e-106">Obter usuário por ID</span><span class="sxs-lookup"><span data-stu-id="7e32e-106">Get user by ID</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e32e-107">Localizar usuários</span><span class="sxs-lookup"><span data-stu-id="7e32e-107">Find users</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e32e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e32e-108">DESCRIPTION</span></span>
<span data-ttu-id="7e32e-109">O cmdlet **Get-AzureRmApiManagementUser** Obtém um usuário especificado ou todos os usuários, se nenhum usuário for especificado.</span><span class="sxs-lookup"><span data-stu-id="7e32e-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="7e32e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e32e-110">EXAMPLES</span></span>

### <span data-ttu-id="7e32e-111">Exemplo 1: obter todos os usuários</span><span class="sxs-lookup"><span data-stu-id="7e32e-111">Example 1: Get all users</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="7e32e-112">Esse comando obtém todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="7e32e-112">This command gets all users.</span></span>

### <span data-ttu-id="7e32e-113">Exemplo 2: obter um usuário por ID</span><span class="sxs-lookup"><span data-stu-id="7e32e-113">Example 2: Get a user by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="7e32e-114">Este comando obtém um usuário por ID.</span><span class="sxs-lookup"><span data-stu-id="7e32e-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="7e32e-115">Exemplo: obter usuários pelo sobrenome</span><span class="sxs-lookup"><span data-stu-id="7e32e-115">Example: Get users by last name</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="7e32e-116">Esse comando obtém os usuários que têm um sobrenome especificado, o mais completo.</span><span class="sxs-lookup"><span data-stu-id="7e32e-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="7e32e-117">Exemplo 4: obter um usuário por endereço de email</span><span class="sxs-lookup"><span data-stu-id="7e32e-117">Example 4: Get a user by email address</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email 
"user@contoso.com"
```

<span data-ttu-id="7e32e-118">Esse comando obtém o usuário que tem o endereço de email especificado.</span><span class="sxs-lookup"><span data-stu-id="7e32e-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="7e32e-119">Exemplo 5: obter todos os usuários de um grupo</span><span class="sxs-lookup"><span data-stu-id="7e32e-119">Example 5: Get all users within a group</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="7e32e-120">Esse comando obtém todos os usuários dentro do grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="7e32e-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="7e32e-121">OS</span><span class="sxs-lookup"><span data-stu-id="7e32e-121">PARAMETERS</span></span>

### <span data-ttu-id="7e32e-122">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7e32e-122">-Context</span></span>
<span data-ttu-id="7e32e-123">Especifica uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="7e32e-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e32e-124">-Email</span><span class="sxs-lookup"><span data-stu-id="7e32e-124">-Email</span></span>
<span data-ttu-id="7e32e-125">Especifica o endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="7e32e-125">Specifies the email address of the user.</span></span>
<span data-ttu-id="7e32e-126">Se esse parâmetro for especificado, esse cmdlet localizará um usuário por email.</span><span class="sxs-lookup"><span data-stu-id="7e32e-126">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="7e32e-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7e32e-127">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e32e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e32e-128">-FirstName</span></span>
<span data-ttu-id="7e32e-129">Especifica o primeiro nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="7e32e-129">Specifies the first name of the user.</span></span>
<span data-ttu-id="7e32e-130">Se esse parâmetro for especificado, esse cmdlet localizará um usuário por nome.</span><span class="sxs-lookup"><span data-stu-id="7e32e-130">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="7e32e-131">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7e32e-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e32e-132">-GroupId</span><span class="sxs-lookup"><span data-stu-id="7e32e-132">-GroupId</span></span>
<span data-ttu-id="7e32e-133">Especifica o identificador do grupo.</span><span class="sxs-lookup"><span data-stu-id="7e32e-133">Specifies the group identifier.</span></span>
<span data-ttu-id="7e32e-134">Se especificado, esse cmdlet localiza todos os usuários dentro do grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="7e32e-134">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="7e32e-135">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7e32e-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e32e-136">-LastName</span><span class="sxs-lookup"><span data-stu-id="7e32e-136">-LastName</span></span>
<span data-ttu-id="7e32e-137">Especifica o último nome de um usuário.</span><span class="sxs-lookup"><span data-stu-id="7e32e-137">Specifies the last name of a user.</span></span>
<span data-ttu-id="7e32e-138">Se especificado, esse cmdlet localiza os usuários por sobrenome.</span><span class="sxs-lookup"><span data-stu-id="7e32e-138">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="7e32e-139">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7e32e-139">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e32e-140">-Estado</span><span class="sxs-lookup"><span data-stu-id="7e32e-140">-State</span></span>
<span data-ttu-id="7e32e-141">Especifica o estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="7e32e-141">Specifies the user state.</span></span>
<span data-ttu-id="7e32e-142">Se especificado, esse cmdlet localiza os usuários nesse estado.</span><span class="sxs-lookup"><span data-stu-id="7e32e-142">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="7e32e-143">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7e32e-143">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: Find users
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e32e-144">-UserId</span><span class="sxs-lookup"><span data-stu-id="7e32e-144">-UserId</span></span>
<span data-ttu-id="7e32e-145">Especifica uma ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="7e32e-145">Specifies a user ID.</span></span>
<span data-ttu-id="7e32e-146">Se especificado, esse cmdlet localiza o usuário por esse identificador.</span><span class="sxs-lookup"><span data-stu-id="7e32e-146">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="7e32e-147">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7e32e-147">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get user by ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e32e-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e32e-148">-DefaultProfile</span></span>
<span data-ttu-id="7e32e-149">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e32e-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e32e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e32e-150">CommonParameters</span></span>
<span data-ttu-id="7e32e-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e32e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e32e-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e32e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e32e-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e32e-153">INPUTS</span></span>

## <span data-ttu-id="7e32e-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e32e-154">OUTPUTS</span></span>

### <span data-ttu-id="7e32e-155">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUser></span><span class="sxs-lookup"><span data-stu-id="7e32e-155">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>

## <span data-ttu-id="7e32e-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e32e-156">NOTES</span></span>

## <span data-ttu-id="7e32e-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e32e-157">RELATED LINKS</span></span>

[<span data-ttu-id="7e32e-158">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7e32e-158">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="7e32e-159">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7e32e-159">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="7e32e-160">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7e32e-160">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


