---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 6cc922ceb09509e70a4017241dc6beb6e5443d1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125678"
---
# <span data-ttu-id="993ca-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="993ca-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="993ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="993ca-102">SYNOPSIS</span></span>
<span data-ttu-id="993ca-103">Registra um novo usuário.</span><span class="sxs-lookup"><span data-stu-id="993ca-103">Registers a new user.</span></span>

## <span data-ttu-id="993ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="993ca-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="993ca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="993ca-105">DESCRIPTION</span></span>
<span data-ttu-id="993ca-106">O cmdlet **New-AzApiManagementUser** registra um novo usuário.</span><span class="sxs-lookup"><span data-stu-id="993ca-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="993ca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="993ca-107">EXAMPLES</span></span>

### <span data-ttu-id="993ca-108">Exemplo 1: registrar um novo usuário</span><span class="sxs-lookup"><span data-stu-id="993ca-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="993ca-109">Esse comando registra um novo usuário chamado Patti Pereira.</span><span class="sxs-lookup"><span data-stu-id="993ca-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="993ca-110">OS</span><span class="sxs-lookup"><span data-stu-id="993ca-110">PARAMETERS</span></span>

### <span data-ttu-id="993ca-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="993ca-111">-Context</span></span>
<span data-ttu-id="993ca-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="993ca-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="993ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="993ca-113">-DefaultProfile</span></span>
<span data-ttu-id="993ca-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="993ca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="993ca-115">-Email</span><span class="sxs-lookup"><span data-stu-id="993ca-115">-Email</span></span>
<span data-ttu-id="993ca-116">Especifica o endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="993ca-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="993ca-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="993ca-117">-FirstName</span></span>
<span data-ttu-id="993ca-118">Especifica o primeiro nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="993ca-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="993ca-119">Esse parâmetro deve ter de 1 a 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="993ca-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="993ca-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="993ca-120">-LastName</span></span>
<span data-ttu-id="993ca-121">Especifica o último nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="993ca-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="993ca-122">Esse parâmetro deve ter de 1 a 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="993ca-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="993ca-123">-Nota</span><span class="sxs-lookup"><span data-stu-id="993ca-123">-Note</span></span>
<span data-ttu-id="993ca-124">Especifica uma observação sobre o usuário.</span><span class="sxs-lookup"><span data-stu-id="993ca-124">Specifies a note about the user.</span></span>
<span data-ttu-id="993ca-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="993ca-125">This parameter is optional.</span></span>
<span data-ttu-id="993ca-126">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="993ca-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="993ca-127">-Senha</span><span class="sxs-lookup"><span data-stu-id="993ca-127">-Password</span></span>
<span data-ttu-id="993ca-128">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="993ca-128">Specifies the user password.</span></span>
<span data-ttu-id="993ca-129">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="993ca-129">This parameter is required.</span></span>

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

### <span data-ttu-id="993ca-130">-Estado</span><span class="sxs-lookup"><span data-stu-id="993ca-130">-State</span></span>
<span data-ttu-id="993ca-131">Especifica o estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="993ca-131">Specifies the user state.</span></span>
<span data-ttu-id="993ca-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="993ca-132">This parameter is optional.</span></span>
<span data-ttu-id="993ca-133">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="993ca-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="993ca-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="993ca-134">-UserId</span></span>
<span data-ttu-id="993ca-135">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="993ca-135">Specifies the user ID.</span></span>
<span data-ttu-id="993ca-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="993ca-136">This parameter is optional.</span></span>
<span data-ttu-id="993ca-137">Se esse parâmetro não for especificado, esse cmdlet gerará uma ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="993ca-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="993ca-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="993ca-138">CommonParameters</span></span>
<span data-ttu-id="993ca-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="993ca-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="993ca-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="993ca-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="993ca-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="993ca-141">INPUTS</span></span>

### <span data-ttu-id="993ca-142">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="993ca-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="993ca-143">System. String</span><span class="sxs-lookup"><span data-stu-id="993ca-143">System.String</span></span>

### <span data-ttu-id="993ca-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="993ca-144">System.Security.SecureString</span></span>

### <span data-ttu-id="993ca-145">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementUserState, Microsoft. Azure. PowerShell. cmdlets. ApiManagement. immanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="993ca-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="993ca-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="993ca-146">OUTPUTS</span></span>

### <span data-ttu-id="993ca-147">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="993ca-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="993ca-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="993ca-148">NOTES</span></span>

## <span data-ttu-id="993ca-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="993ca-149">RELATED LINKS</span></span>

[<span data-ttu-id="993ca-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="993ca-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="993ca-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="993ca-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


