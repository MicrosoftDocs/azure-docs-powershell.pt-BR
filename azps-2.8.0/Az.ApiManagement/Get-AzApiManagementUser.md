---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 6a242334378ceade2f786873181c68f04f8b09a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598084"
---
# <span data-ttu-id="f9736-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f9736-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="f9736-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9736-102">SYNOPSIS</span></span>
<span data-ttu-id="f9736-103">Obtém um ou mais usuários.</span><span class="sxs-lookup"><span data-stu-id="f9736-103">Gets a user or users.</span></span>

## <span data-ttu-id="f9736-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9736-104">SYNTAX</span></span>

### <span data-ttu-id="f9736-105">GeAllUsers (padrão)</span><span class="sxs-lookup"><span data-stu-id="f9736-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9736-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="f9736-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9736-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="f9736-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9736-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9736-108">DESCRIPTION</span></span>
<span data-ttu-id="f9736-109">O cmdlet **Get-AzApiManagementUser** Obtém um usuário especificado ou todos os usuários, se nenhum usuário for especificado.</span><span class="sxs-lookup"><span data-stu-id="f9736-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="f9736-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9736-110">EXAMPLES</span></span>

### <span data-ttu-id="f9736-111">Exemplo 1: obter todos os usuários</span><span class="sxs-lookup"><span data-stu-id="f9736-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="f9736-112">Esse comando obtém todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="f9736-112">This command gets all users.</span></span>

### <span data-ttu-id="f9736-113">Exemplo 2: obter um usuário por ID</span><span class="sxs-lookup"><span data-stu-id="f9736-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="f9736-114">Este comando obtém um usuário por ID.</span><span class="sxs-lookup"><span data-stu-id="f9736-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="f9736-115">Exemplo: obter usuários pelo sobrenome</span><span class="sxs-lookup"><span data-stu-id="f9736-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="f9736-116">Esse comando obtém os usuários que têm um sobrenome especificado, o mais completo.</span><span class="sxs-lookup"><span data-stu-id="f9736-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="f9736-117">Exemplo 4: obter um usuário por endereço de email</span><span class="sxs-lookup"><span data-stu-id="f9736-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="f9736-118">Esse comando obtém o usuário que tem o endereço de email especificado.</span><span class="sxs-lookup"><span data-stu-id="f9736-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="f9736-119">Exemplo 5: obter todos os usuários de um grupo</span><span class="sxs-lookup"><span data-stu-id="f9736-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="f9736-120">Esse comando obtém todos os usuários dentro do grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="f9736-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="f9736-121">OS</span><span class="sxs-lookup"><span data-stu-id="f9736-121">PARAMETERS</span></span>

### <span data-ttu-id="f9736-122">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f9736-122">-Context</span></span>
<span data-ttu-id="f9736-123">Especifica uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="f9736-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9736-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9736-124">-DefaultProfile</span></span>
<span data-ttu-id="f9736-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9736-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9736-126">-Email</span><span class="sxs-lookup"><span data-stu-id="f9736-126">-Email</span></span>
<span data-ttu-id="f9736-127">Especifica o endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="f9736-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="f9736-128">Se esse parâmetro for especificado, esse cmdlet localizará um usuário por email.</span><span class="sxs-lookup"><span data-stu-id="f9736-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="f9736-129">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f9736-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="f9736-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9736-130">-FirstName</span></span>
<span data-ttu-id="f9736-131">Especifica o primeiro nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="f9736-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="f9736-132">Se esse parâmetro for especificado, esse cmdlet localizará um usuário por nome.</span><span class="sxs-lookup"><span data-stu-id="f9736-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="f9736-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f9736-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="f9736-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f9736-134">-GroupId</span></span>
<span data-ttu-id="f9736-135">Especifica o identificador do grupo.</span><span class="sxs-lookup"><span data-stu-id="f9736-135">Specifies the group identifier.</span></span>
<span data-ttu-id="f9736-136">Se especificado, esse cmdlet localiza todos os usuários dentro do grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="f9736-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="f9736-137">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f9736-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="f9736-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="f9736-138">-LastName</span></span>
<span data-ttu-id="f9736-139">Especifica o último nome de um usuário.</span><span class="sxs-lookup"><span data-stu-id="f9736-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="f9736-140">Se especificado, esse cmdlet localiza os usuários por sobrenome.</span><span class="sxs-lookup"><span data-stu-id="f9736-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="f9736-141">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f9736-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="f9736-142">-Estado</span><span class="sxs-lookup"><span data-stu-id="f9736-142">-State</span></span>
<span data-ttu-id="f9736-143">Especifica o estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="f9736-143">Specifies the user state.</span></span>
<span data-ttu-id="f9736-144">Se especificado, esse cmdlet localiza os usuários nesse estado.</span><span class="sxs-lookup"><span data-stu-id="f9736-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="f9736-145">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f9736-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="f9736-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="f9736-146">-UserId</span></span>
<span data-ttu-id="f9736-147">Especifica uma ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="f9736-147">Specifies a user ID.</span></span>
<span data-ttu-id="f9736-148">Se especificado, esse cmdlet localiza o usuário por esse identificador.</span><span class="sxs-lookup"><span data-stu-id="f9736-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="f9736-149">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f9736-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="f9736-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9736-150">CommonParameters</span></span>
<span data-ttu-id="f9736-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9736-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9736-152">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9736-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9736-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9736-153">INPUTS</span></span>

### <span data-ttu-id="f9736-154">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f9736-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f9736-155">System. String</span><span class="sxs-lookup"><span data-stu-id="f9736-155">System.String</span></span>

### <span data-ttu-id="f9736-156">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementUserState, Microsoft. Azure. PowerShell. cmdlets. ApiManagement. immanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f9736-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f9736-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9736-157">OUTPUTS</span></span>

### <span data-ttu-id="f9736-158">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f9736-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="f9736-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9736-159">NOTES</span></span>

## <span data-ttu-id="f9736-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9736-160">RELATED LINKS</span></span>

[<span data-ttu-id="f9736-161">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f9736-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="f9736-162">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f9736-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="f9736-163">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f9736-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


