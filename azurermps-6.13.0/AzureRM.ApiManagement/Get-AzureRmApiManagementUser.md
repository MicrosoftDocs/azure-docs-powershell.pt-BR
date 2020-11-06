---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: 8f02b88115ec6dc415ecf6cf5464503d61778cca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431472"
---
# <span data-ttu-id="0315a-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0315a-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="0315a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0315a-102">SYNOPSIS</span></span>
<span data-ttu-id="0315a-103">Obtém um ou mais usuários.</span><span class="sxs-lookup"><span data-stu-id="0315a-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0315a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0315a-104">SYNTAX</span></span>

### <span data-ttu-id="0315a-105">GeAllUsers (padrão)</span><span class="sxs-lookup"><span data-stu-id="0315a-105">GeAllUsers (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0315a-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="0315a-106">GetByUserId</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0315a-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="0315a-107">GetByUser</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0315a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0315a-108">DESCRIPTION</span></span>
<span data-ttu-id="0315a-109">O cmdlet **Get-AzureRmApiManagementUser** Obtém um usuário especificado ou todos os usuários, se nenhum usuário for especificado.</span><span class="sxs-lookup"><span data-stu-id="0315a-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="0315a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0315a-110">EXAMPLES</span></span>

### <span data-ttu-id="0315a-111">Exemplo 1: obter todos os usuários</span><span class="sxs-lookup"><span data-stu-id="0315a-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="0315a-112">Esse comando obtém todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="0315a-112">This command gets all users.</span></span>

### <span data-ttu-id="0315a-113">Exemplo 2: obter um usuário por ID</span><span class="sxs-lookup"><span data-stu-id="0315a-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="0315a-114">Este comando obtém um usuário por ID.</span><span class="sxs-lookup"><span data-stu-id="0315a-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="0315a-115">Exemplo: obter usuários pelo sobrenome</span><span class="sxs-lookup"><span data-stu-id="0315a-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="0315a-116">Esse comando obtém os usuários que têm um sobrenome especificado, o mais completo.</span><span class="sxs-lookup"><span data-stu-id="0315a-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="0315a-117">Exemplo 4: obter um usuário por endereço de email</span><span class="sxs-lookup"><span data-stu-id="0315a-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="0315a-118">Esse comando obtém o usuário que tem o endereço de email especificado.</span><span class="sxs-lookup"><span data-stu-id="0315a-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="0315a-119">Exemplo 5: obter todos os usuários de um grupo</span><span class="sxs-lookup"><span data-stu-id="0315a-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="0315a-120">Esse comando obtém todos os usuários dentro do grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="0315a-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="0315a-121">OS</span><span class="sxs-lookup"><span data-stu-id="0315a-121">PARAMETERS</span></span>

### <span data-ttu-id="0315a-122">-Contexto</span><span class="sxs-lookup"><span data-stu-id="0315a-122">-Context</span></span>
<span data-ttu-id="0315a-123">Especifica uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="0315a-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="0315a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0315a-124">-DefaultProfile</span></span>
<span data-ttu-id="0315a-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0315a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0315a-126">-Email</span><span class="sxs-lookup"><span data-stu-id="0315a-126">-Email</span></span>
<span data-ttu-id="0315a-127">Especifica o endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="0315a-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="0315a-128">Se esse parâmetro for especificado, esse cmdlet localizará um usuário por email.</span><span class="sxs-lookup"><span data-stu-id="0315a-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="0315a-129">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0315a-129">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0315a-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="0315a-130">-FirstName</span></span>
<span data-ttu-id="0315a-131">Especifica o primeiro nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="0315a-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="0315a-132">Se esse parâmetro for especificado, esse cmdlet localizará um usuário por nome.</span><span class="sxs-lookup"><span data-stu-id="0315a-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="0315a-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0315a-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0315a-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="0315a-134">-GroupId</span></span>
<span data-ttu-id="0315a-135">Especifica o identificador do grupo.</span><span class="sxs-lookup"><span data-stu-id="0315a-135">Specifies the group identifier.</span></span>
<span data-ttu-id="0315a-136">Se especificado, esse cmdlet localiza todos os usuários dentro do grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="0315a-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="0315a-137">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0315a-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0315a-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="0315a-138">-LastName</span></span>
<span data-ttu-id="0315a-139">Especifica o último nome de um usuário.</span><span class="sxs-lookup"><span data-stu-id="0315a-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="0315a-140">Se especificado, esse cmdlet localiza os usuários por sobrenome.</span><span class="sxs-lookup"><span data-stu-id="0315a-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="0315a-141">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0315a-141">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0315a-142">-Estado</span><span class="sxs-lookup"><span data-stu-id="0315a-142">-State</span></span>
<span data-ttu-id="0315a-143">Especifica o estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="0315a-143">Specifies the user state.</span></span>
<span data-ttu-id="0315a-144">Se especificado, esse cmdlet localiza os usuários nesse estado.</span><span class="sxs-lookup"><span data-stu-id="0315a-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="0315a-145">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0315a-145">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: GetByUser
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0315a-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="0315a-146">-UserId</span></span>
<span data-ttu-id="0315a-147">Especifica uma ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="0315a-147">Specifies a user ID.</span></span>
<span data-ttu-id="0315a-148">Se especificado, esse cmdlet localiza o usuário por esse identificador.</span><span class="sxs-lookup"><span data-stu-id="0315a-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="0315a-149">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0315a-149">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0315a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0315a-150">CommonParameters</span></span>
<span data-ttu-id="0315a-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0315a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0315a-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0315a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0315a-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0315a-153">INPUTS</span></span>

### <span data-ttu-id="0315a-154">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0315a-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0315a-155">System. String</span><span class="sxs-lookup"><span data-stu-id="0315a-155">System.String</span></span>

### <span data-ttu-id="0315a-156">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementUserState, Microsoft. Azure. Commands. ApiManagement. onmanagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0315a-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0315a-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0315a-157">OUTPUTS</span></span>

### <span data-ttu-id="0315a-158">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0315a-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="0315a-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0315a-159">NOTES</span></span>

## <span data-ttu-id="0315a-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0315a-160">RELATED LINKS</span></span>

[<span data-ttu-id="0315a-161">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0315a-161">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="0315a-162">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0315a-162">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="0315a-163">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0315a-163">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


