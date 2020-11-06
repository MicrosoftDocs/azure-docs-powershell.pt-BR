---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: fa7b44710aa51a138729d9a04a41a82ec2769f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611071"
---
# <span data-ttu-id="169b3-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="169b3-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="169b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="169b3-102">SYNOPSIS</span></span>
<span data-ttu-id="169b3-103">Registra um novo usuário.</span><span class="sxs-lookup"><span data-stu-id="169b3-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="169b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="169b3-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="169b3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="169b3-105">DESCRIPTION</span></span>
<span data-ttu-id="169b3-106">O cmdlet **New-AzureRmApiManagementUser** registra um novo usuário.</span><span class="sxs-lookup"><span data-stu-id="169b3-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="169b3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="169b3-107">EXAMPLES</span></span>

### <span data-ttu-id="169b3-108">Exemplo 1: registrar um novo usuário</span><span class="sxs-lookup"><span data-stu-id="169b3-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="169b3-109">Esse comando registra um novo usuário chamado Patti Pereira.</span><span class="sxs-lookup"><span data-stu-id="169b3-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="169b3-110">OS</span><span class="sxs-lookup"><span data-stu-id="169b3-110">PARAMETERS</span></span>

### <span data-ttu-id="169b3-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="169b3-111">-Context</span></span>
<span data-ttu-id="169b3-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="169b3-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="169b3-113">-DefaultProfile</span></span>
<span data-ttu-id="169b3-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="169b3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169b3-115">-Email</span><span class="sxs-lookup"><span data-stu-id="169b3-115">-Email</span></span>
<span data-ttu-id="169b3-116">Especifica o endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="169b3-116">Specifies the email address of the user.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169b3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="169b3-117">-FirstName</span></span>
<span data-ttu-id="169b3-118">Especifica o primeiro nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="169b3-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="169b3-119">Esse parâmetro deve ter de 1 a 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="169b3-119">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169b3-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="169b3-120">-LastName</span></span>
<span data-ttu-id="169b3-121">Especifica o último nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="169b3-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="169b3-122">Esse parâmetro deve ter de 1 a 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="169b3-122">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169b3-123">-Nota</span><span class="sxs-lookup"><span data-stu-id="169b3-123">-Note</span></span>
<span data-ttu-id="169b3-124">Especifica uma observação sobre o usuário.</span><span class="sxs-lookup"><span data-stu-id="169b3-124">Specifies a note about the user.</span></span>
<span data-ttu-id="169b3-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="169b3-125">This parameter is optional.</span></span>
<span data-ttu-id="169b3-126">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="169b3-126">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169b3-127">-Senha</span><span class="sxs-lookup"><span data-stu-id="169b3-127">-Password</span></span>
<span data-ttu-id="169b3-128">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="169b3-128">Specifies the user password.</span></span>
<span data-ttu-id="169b3-129">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="169b3-129">This parameter is required.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169b3-130">-Estado</span><span class="sxs-lookup"><span data-stu-id="169b3-130">-State</span></span>
<span data-ttu-id="169b3-131">Especifica o estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="169b3-131">Specifies the user state.</span></span>
<span data-ttu-id="169b3-132">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="169b3-132">This parameter is optional.</span></span>
<span data-ttu-id="169b3-133">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="169b3-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169b3-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="169b3-134">-UserId</span></span>
<span data-ttu-id="169b3-135">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="169b3-135">Specifies the user ID.</span></span>
<span data-ttu-id="169b3-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="169b3-136">This parameter is optional.</span></span>
<span data-ttu-id="169b3-137">Se esse parâmetro não for especificado, esse cmdlet gerará uma ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="169b3-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169b3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169b3-138">CommonParameters</span></span>
<span data-ttu-id="169b3-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="169b3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169b3-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="169b3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169b3-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="169b3-141">INPUTS</span></span>

### <span data-ttu-id="169b3-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="169b3-142">None</span></span>
<span data-ttu-id="169b3-143">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="169b3-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="169b3-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="169b3-144">OUTPUTS</span></span>

### <span data-ttu-id="169b3-145">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="169b3-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="169b3-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="169b3-146">NOTES</span></span>

## <span data-ttu-id="169b3-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="169b3-147">RELATED LINKS</span></span>

[<span data-ttu-id="169b3-148">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="169b3-148">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="169b3-149">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="169b3-149">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


