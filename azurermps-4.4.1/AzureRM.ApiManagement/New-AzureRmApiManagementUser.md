---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 93e6ce5a96afd1c3b297d6296c3491445593d430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431839"
---
# <span data-ttu-id="848eb-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="848eb-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="848eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="848eb-102">SYNOPSIS</span></span>
<span data-ttu-id="848eb-103">Registra um novo usuário.</span><span class="sxs-lookup"><span data-stu-id="848eb-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="848eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="848eb-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <String> [-State <PsApiManagementUserState>] [-Note <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="848eb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="848eb-105">DESCRIPTION</span></span>
<span data-ttu-id="848eb-106">O cmdlet **New-AzureRmApiManagementUser** registra um novo usuário.</span><span class="sxs-lookup"><span data-stu-id="848eb-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="848eb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="848eb-107">EXAMPLES</span></span>

### <span data-ttu-id="848eb-108">Exemplo 1: registrar um novo usuário</span><span class="sxs-lookup"><span data-stu-id="848eb-108">Example 1: Register a new user</span></span>
```
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password "qwerty"
```

<span data-ttu-id="848eb-109">Esse comando registra um novo usuário chamado Patti Pereira.</span><span class="sxs-lookup"><span data-stu-id="848eb-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="848eb-110">OS</span><span class="sxs-lookup"><span data-stu-id="848eb-110">PARAMETERS</span></span>

### <span data-ttu-id="848eb-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="848eb-111">-Context</span></span>
<span data-ttu-id="848eb-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="848eb-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="848eb-113">-Email</span><span class="sxs-lookup"><span data-stu-id="848eb-113">-Email</span></span>
<span data-ttu-id="848eb-114">Especifica o endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="848eb-114">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="848eb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="848eb-115">-FirstName</span></span>
<span data-ttu-id="848eb-116">Especifica o primeiro nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="848eb-116">Specifies the first name of the user.</span></span>
<span data-ttu-id="848eb-117">Esse parâmetro deve ter de 1 a 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="848eb-117">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="848eb-118">-LastName</span><span class="sxs-lookup"><span data-stu-id="848eb-118">-LastName</span></span>
<span data-ttu-id="848eb-119">Especifica o último nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="848eb-119">Specifies the last name of the user.</span></span>
<span data-ttu-id="848eb-120">Esse parâmetro deve ter de 1 a 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="848eb-120">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="848eb-121">-Nota</span><span class="sxs-lookup"><span data-stu-id="848eb-121">-Note</span></span>
<span data-ttu-id="848eb-122">Especifica uma observação sobre o usuário.</span><span class="sxs-lookup"><span data-stu-id="848eb-122">Specifies a note about the user.</span></span>
<span data-ttu-id="848eb-123">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="848eb-123">This parameter is optional.</span></span>
<span data-ttu-id="848eb-124">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="848eb-124">The default value is $Null.</span></span>

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

### <span data-ttu-id="848eb-125">-Senha</span><span class="sxs-lookup"><span data-stu-id="848eb-125">-Password</span></span>
<span data-ttu-id="848eb-126">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="848eb-126">Specifies the user password.</span></span>
<span data-ttu-id="848eb-127">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="848eb-127">This parameter is required.</span></span>

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

### <span data-ttu-id="848eb-128">-Estado</span><span class="sxs-lookup"><span data-stu-id="848eb-128">-State</span></span>
<span data-ttu-id="848eb-129">Especifica o estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="848eb-129">Specifies the user state.</span></span>
<span data-ttu-id="848eb-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="848eb-130">This parameter is optional.</span></span>
<span data-ttu-id="848eb-131">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="848eb-131">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848eb-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="848eb-132">-UserId</span></span>
<span data-ttu-id="848eb-133">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="848eb-133">Specifies the user ID.</span></span>
<span data-ttu-id="848eb-134">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="848eb-134">This parameter is optional.</span></span>
<span data-ttu-id="848eb-135">Se esse parâmetro não for especificado, esse cmdlet gerará uma ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="848eb-135">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="848eb-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="848eb-136">-DefaultProfile</span></span>
<span data-ttu-id="848eb-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="848eb-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="848eb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="848eb-138">CommonParameters</span></span>
<span data-ttu-id="848eb-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="848eb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="848eb-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="848eb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="848eb-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="848eb-141">INPUTS</span></span>

## <span data-ttu-id="848eb-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="848eb-142">OUTPUTS</span></span>

### <span data-ttu-id="848eb-143">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="848eb-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="848eb-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="848eb-144">NOTES</span></span>

## <span data-ttu-id="848eb-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="848eb-145">RELATED LINKS</span></span>

[<span data-ttu-id="848eb-146">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="848eb-146">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="848eb-147">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="848eb-147">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


