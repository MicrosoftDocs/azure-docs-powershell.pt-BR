---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 1c8b7f8069c63d18f69285f7e40ac4d652f0bf73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602497"
---
# <span data-ttu-id="dc275-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="dc275-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="dc275-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc275-102">SYNOPSIS</span></span>
<span data-ttu-id="dc275-103">Registra um novo usuário.</span><span class="sxs-lookup"><span data-stu-id="dc275-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc275-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc275-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc275-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc275-105">DESCRIPTION</span></span>
<span data-ttu-id="dc275-106">O cmdlet **New-AzureRmApiManagementUser** registra um novo usuário.</span><span class="sxs-lookup"><span data-stu-id="dc275-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="dc275-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc275-107">EXAMPLES</span></span>

### <span data-ttu-id="dc275-108">Exemplo 1: registrar um novo usuário</span><span class="sxs-lookup"><span data-stu-id="dc275-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="dc275-109">Esse comando registra um novo usuário chamado Patti Pereira.</span><span class="sxs-lookup"><span data-stu-id="dc275-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="dc275-110">OS</span><span class="sxs-lookup"><span data-stu-id="dc275-110">PARAMETERS</span></span>

### <span data-ttu-id="dc275-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="dc275-111">-Context</span></span>
<span data-ttu-id="dc275-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="dc275-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dc275-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc275-113">-DefaultProfile</span></span>
<span data-ttu-id="dc275-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc275-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc275-115">-Email</span><span class="sxs-lookup"><span data-stu-id="dc275-115">-Email</span></span>
<span data-ttu-id="dc275-116">Especifica o endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc275-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="dc275-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc275-117">-FirstName</span></span>
<span data-ttu-id="dc275-118">Especifica o primeiro nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc275-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="dc275-119">Esse parâmetro deve ter de 1 a 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="dc275-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="dc275-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="dc275-120">-LastName</span></span>
<span data-ttu-id="dc275-121">Especifica o último nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc275-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="dc275-122">Esse parâmetro deve ter de 1 a 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="dc275-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="dc275-123">-Nota</span><span class="sxs-lookup"><span data-stu-id="dc275-123">-Note</span></span>
<span data-ttu-id="dc275-124">Especifica uma observação sobre o usuário.</span><span class="sxs-lookup"><span data-stu-id="dc275-124">Specifies a note about the user.</span></span>
<span data-ttu-id="dc275-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="dc275-125">This parameter is optional.</span></span>
<span data-ttu-id="dc275-126">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="dc275-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="dc275-127">-Senha</span><span class="sxs-lookup"><span data-stu-id="dc275-127">-Password</span></span>
<span data-ttu-id="dc275-128">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc275-128">Specifies the user password.</span></span>
<span data-ttu-id="dc275-129">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="dc275-129">This parameter is required.</span></span>

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

### <span data-ttu-id="dc275-130">-Estado</span><span class="sxs-lookup"><span data-stu-id="dc275-130">-State</span></span>
<span data-ttu-id="dc275-131">Especifica o estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc275-131">Specifies the user state.</span></span>
<span data-ttu-id="dc275-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="dc275-132">This parameter is optional.</span></span>
<span data-ttu-id="dc275-133">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="dc275-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="dc275-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="dc275-134">-UserId</span></span>
<span data-ttu-id="dc275-135">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="dc275-135">Specifies the user ID.</span></span>
<span data-ttu-id="dc275-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="dc275-136">This parameter is optional.</span></span>
<span data-ttu-id="dc275-137">Se esse parâmetro não for especificado, esse cmdlet gerará uma ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="dc275-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="dc275-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc275-138">CommonParameters</span></span>
<span data-ttu-id="dc275-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc275-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc275-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc275-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc275-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc275-141">INPUTS</span></span>

### <span data-ttu-id="dc275-142">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dc275-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dc275-143">System. String</span><span class="sxs-lookup"><span data-stu-id="dc275-143">System.String</span></span>

### <span data-ttu-id="dc275-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="dc275-144">System.Security.SecureString</span></span>

### <span data-ttu-id="dc275-145">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementUserState, Microsoft. Azure. Commands. ApiManagement. onmanagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dc275-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dc275-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc275-146">OUTPUTS</span></span>

### <span data-ttu-id="dc275-147">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="dc275-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="dc275-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc275-148">NOTES</span></span>

## <span data-ttu-id="dc275-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc275-149">RELATED LINKS</span></span>

[<span data-ttu-id="dc275-150">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="dc275-150">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="dc275-151">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="dc275-151">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


