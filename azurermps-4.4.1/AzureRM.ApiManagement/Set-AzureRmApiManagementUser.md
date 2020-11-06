---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: a9d36dca9894a10c76f2ca5a96880f4aafecb5e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427013"
---
# <span data-ttu-id="ece55-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ece55-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="ece55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ece55-102">SYNOPSIS</span></span>
<span data-ttu-id="ece55-103">Define detalhes do usuário.</span><span class="sxs-lookup"><span data-stu-id="ece55-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ece55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ece55-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <String>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ece55-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ece55-105">DESCRIPTION</span></span>
<span data-ttu-id="ece55-106">O cmdlet **set-AzureRmApiManagementUser** define detalhes do usuário.</span><span class="sxs-lookup"><span data-stu-id="ece55-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="ece55-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ece55-107">EXAMPLES</span></span>

### <span data-ttu-id="ece55-108">Exemplo 1: alterar a senha de um usuário, o endereço de email e o estado</span><span class="sxs-lookup"><span data-stu-id="ece55-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password "asdfgh" -State "Blocked"
```

<span data-ttu-id="ece55-109">Esse comando define uma nova senha de usuário e um endereço de email e bloqueia o usuário.</span><span class="sxs-lookup"><span data-stu-id="ece55-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="ece55-110">OS</span><span class="sxs-lookup"><span data-stu-id="ece55-110">PARAMETERS</span></span>

### <span data-ttu-id="ece55-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ece55-111">-Context</span></span>
<span data-ttu-id="ece55-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ece55-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="ece55-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ece55-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ece55-114">-Email</span><span class="sxs-lookup"><span data-stu-id="ece55-114">-Email</span></span>
<span data-ttu-id="ece55-115">Especifica o endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="ece55-115">Specifies the email address of the user.</span></span>
<span data-ttu-id="ece55-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ece55-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="ece55-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ece55-117">-FirstName</span></span>
<span data-ttu-id="ece55-118">Especifica o primeiro nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="ece55-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="ece55-119">Esse parâmetro deve ter de 1 a 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="ece55-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="ece55-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="ece55-120">-LastName</span></span>
<span data-ttu-id="ece55-121">Especifica o último nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="ece55-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="ece55-122">Esse parâmetro deve ter entre 1 e 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="ece55-122">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="ece55-123">-Nota</span><span class="sxs-lookup"><span data-stu-id="ece55-123">-Note</span></span>
<span data-ttu-id="ece55-124">Especifica uma observação sobre o usuário.</span><span class="sxs-lookup"><span data-stu-id="ece55-124">Specifies a note about the user.</span></span>
<span data-ttu-id="ece55-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ece55-125">This parameter is optional.</span></span>
<span data-ttu-id="ece55-126">O valor padrão desse parâmetro é $null.</span><span class="sxs-lookup"><span data-stu-id="ece55-126">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="ece55-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ece55-127">-PassThru</span></span>
<span data-ttu-id="ece55-128">PassThru</span><span class="sxs-lookup"><span data-stu-id="ece55-128">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece55-129">-Senha</span><span class="sxs-lookup"><span data-stu-id="ece55-129">-Password</span></span>
<span data-ttu-id="ece55-130">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="ece55-130">Specifies the user password.</span></span>
<span data-ttu-id="ece55-131">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ece55-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="ece55-132">-Estado</span><span class="sxs-lookup"><span data-stu-id="ece55-132">-State</span></span>
<span data-ttu-id="ece55-133">Especifica o estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="ece55-133">Specifies the user state.</span></span>
<span data-ttu-id="ece55-134">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ece55-134">This parameter is optional.</span></span>
<span data-ttu-id="ece55-135">O valor padrão é ativo.</span><span class="sxs-lookup"><span data-stu-id="ece55-135">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece55-136">-UserId</span><span class="sxs-lookup"><span data-stu-id="ece55-136">-UserId</span></span>
<span data-ttu-id="ece55-137">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="ece55-137">Specifies the user ID.</span></span>
<span data-ttu-id="ece55-138">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ece55-138">This parameter is required.</span></span>

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

### <span data-ttu-id="ece55-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece55-139">-DefaultProfile</span></span>
<span data-ttu-id="ece55-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ece55-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ece55-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece55-141">CommonParameters</span></span>
<span data-ttu-id="ece55-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece55-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece55-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece55-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece55-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ece55-144">INPUTS</span></span>

## <span data-ttu-id="ece55-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ece55-145">OUTPUTS</span></span>

### <span data-ttu-id="ece55-146">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ece55-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="ece55-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ece55-147">NOTES</span></span>

## <span data-ttu-id="ece55-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ece55-148">RELATED LINKS</span></span>

[<span data-ttu-id="ece55-149">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ece55-149">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="ece55-150">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ece55-150">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="ece55-151">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ece55-151">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


