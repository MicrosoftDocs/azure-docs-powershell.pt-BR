---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 7e141cb5c1bde59bec9e981ffd228dba6db33089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886283"
---
# <span data-ttu-id="0d5ff-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0d5ff-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="0d5ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d5ff-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5ff-103">Registra um novo usuário.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-103">Registers a new user.</span></span>

## <span data-ttu-id="0d5ff-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0d5ff-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d5ff-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0d5ff-105">DESCRIPTION</span></span>
<span data-ttu-id="0d5ff-106">O cmdlet **New-AzApiManagementUser** registra um novo usuário.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="0d5ff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d5ff-107">EXAMPLES</span></span>

### <span data-ttu-id="0d5ff-108">Exemplo 1: Registrar um novo usuário</span><span class="sxs-lookup"><span data-stu-id="0d5ff-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="0d5ff-109">Este comando registra uma nova usuário chamada Patti Fuller.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="0d5ff-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0d5ff-110">PARAMETERS</span></span>

### <span data-ttu-id="0d5ff-111">-Context</span><span class="sxs-lookup"><span data-stu-id="0d5ff-111">-Context</span></span>
<span data-ttu-id="0d5ff-112">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="0d5ff-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0d5ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5ff-113">-DefaultProfile</span></span>
<span data-ttu-id="0d5ff-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d5ff-115">-Email</span><span class="sxs-lookup"><span data-stu-id="0d5ff-115">-Email</span></span>
<span data-ttu-id="0d5ff-116">Especifica o endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-116">Specifies the email address of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5ff-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="0d5ff-117">-FirstName</span></span>
<span data-ttu-id="0d5ff-118">Especifica o primeiro nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="0d5ff-119">Esse parâmetro deve ter de 1 a 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-119">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5ff-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="0d5ff-120">-LastName</span></span>
<span data-ttu-id="0d5ff-121">Especifica o sobrenome do usuário.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="0d5ff-122">Esse parâmetro deve ter de 1 a 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-122">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5ff-123">-Observação</span><span class="sxs-lookup"><span data-stu-id="0d5ff-123">-Note</span></span>
<span data-ttu-id="0d5ff-124">Especifica uma observação sobre o usuário.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-124">Specifies a note about the user.</span></span>
<span data-ttu-id="0d5ff-125">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-125">This parameter is optional.</span></span>
<span data-ttu-id="0d5ff-126">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-126">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5ff-127">-Password</span><span class="sxs-lookup"><span data-stu-id="0d5ff-127">-Password</span></span>
<span data-ttu-id="0d5ff-128">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-128">Specifies the user password.</span></span>
<span data-ttu-id="0d5ff-129">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-129">This parameter is required.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5ff-130">-State</span><span class="sxs-lookup"><span data-stu-id="0d5ff-130">-State</span></span>
<span data-ttu-id="0d5ff-131">Especifica o estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-131">Specifies the user state.</span></span>
<span data-ttu-id="0d5ff-132">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-132">This parameter is optional.</span></span>
<span data-ttu-id="0d5ff-133">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5ff-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="0d5ff-134">-UserId</span></span>
<span data-ttu-id="0d5ff-135">Especifica a ID do usuário.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-135">Specifies the user ID.</span></span>
<span data-ttu-id="0d5ff-136">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-136">This parameter is optional.</span></span>
<span data-ttu-id="0d5ff-137">Se esse parâmetro não for especificado, esse cmdlet gerará uma ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5ff-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5ff-138">CommonParameters</span></span>
<span data-ttu-id="0d5ff-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d5ff-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5ff-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d5ff-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5ff-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d5ff-141">INPUTS</span></span>

### <span data-ttu-id="0d5ff-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0d5ff-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0d5ff-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0d5ff-143">System.String</span></span>

### <span data-ttu-id="0d5ff-144">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="0d5ff-144">System.Security.SecureString</span></span>

### <span data-ttu-id="0d5ff-145">System.Nullable'1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0d5ff-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0d5ff-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0d5ff-146">OUTPUTS</span></span>

### <span data-ttu-id="0d5ff-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0d5ff-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="0d5ff-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="0d5ff-148">NOTES</span></span>

## <span data-ttu-id="0d5ff-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d5ff-149">RELATED LINKS</span></span>

[<span data-ttu-id="0d5ff-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0d5ff-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="0d5ff-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0d5ff-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


