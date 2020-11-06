---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: d3825b4887d2361a4bb378bfddc3085773efd84b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440531"
---
# <span data-ttu-id="a32e4-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a32e4-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="a32e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a32e4-102">SYNOPSIS</span></span>
<span data-ttu-id="a32e4-103">Define detalhes do usuário.</span><span class="sxs-lookup"><span data-stu-id="a32e4-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a32e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a32e4-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a32e4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a32e4-105">DESCRIPTION</span></span>
<span data-ttu-id="a32e4-106">O cmdlet **set-AzureRmApiManagementUser** define detalhes do usuário.</span><span class="sxs-lookup"><span data-stu-id="a32e4-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="a32e4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a32e4-107">EXAMPLES</span></span>

### <span data-ttu-id="a32e4-108">Exemplo 1: alterar a senha de um usuário, o endereço de email e o estado</span><span class="sxs-lookup"><span data-stu-id="a32e4-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="a32e4-109">Esse comando define uma nova senha de usuário e um endereço de email e bloqueia o usuário.</span><span class="sxs-lookup"><span data-stu-id="a32e4-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="a32e4-110">OS</span><span class="sxs-lookup"><span data-stu-id="a32e4-110">PARAMETERS</span></span>

### <span data-ttu-id="a32e4-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a32e4-111">-Context</span></span>
<span data-ttu-id="a32e4-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a32e4-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="a32e4-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a32e4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a32e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32e4-114">-DefaultProfile</span></span>
<span data-ttu-id="a32e4-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a32e4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a32e4-116">-Email</span><span class="sxs-lookup"><span data-stu-id="a32e4-116">-Email</span></span>
<span data-ttu-id="a32e4-117">Especifica o endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="a32e4-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="a32e4-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a32e4-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="a32e4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a32e4-119">-FirstName</span></span>
<span data-ttu-id="a32e4-120">Especifica o primeiro nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="a32e4-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="a32e4-121">Esse parâmetro deve ter de 1 a 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="a32e4-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="a32e4-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="a32e4-122">-LastName</span></span>
<span data-ttu-id="a32e4-123">Especifica o último nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="a32e4-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="a32e4-124">Esse parâmetro deve ter entre 1 e 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="a32e4-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="a32e4-125">-Nota</span><span class="sxs-lookup"><span data-stu-id="a32e4-125">-Note</span></span>
<span data-ttu-id="a32e4-126">Especifica uma observação sobre o usuário.</span><span class="sxs-lookup"><span data-stu-id="a32e4-126">Specifies a note about the user.</span></span>
<span data-ttu-id="a32e4-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a32e4-127">This parameter is optional.</span></span>
<span data-ttu-id="a32e4-128">O valor padrão desse parâmetro é $null.</span><span class="sxs-lookup"><span data-stu-id="a32e4-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="a32e4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a32e4-129">-PassThru</span></span>
<span data-ttu-id="a32e4-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="a32e4-130">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a32e4-131">-Senha</span><span class="sxs-lookup"><span data-stu-id="a32e4-131">-Password</span></span>
<span data-ttu-id="a32e4-132">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="a32e4-132">Specifies the user password.</span></span>
<span data-ttu-id="a32e4-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a32e4-133">This parameter is optional.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a32e4-134">-Estado</span><span class="sxs-lookup"><span data-stu-id="a32e4-134">-State</span></span>
<span data-ttu-id="a32e4-135">Especifica o estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="a32e4-135">Specifies the user state.</span></span>
<span data-ttu-id="a32e4-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a32e4-136">This parameter is optional.</span></span>
<span data-ttu-id="a32e4-137">O valor padrão é ativo.</span><span class="sxs-lookup"><span data-stu-id="a32e4-137">The default value is Active.</span></span>

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

### <span data-ttu-id="a32e4-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="a32e4-138">-UserId</span></span>
<span data-ttu-id="a32e4-139">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="a32e4-139">Specifies the user ID.</span></span>
<span data-ttu-id="a32e4-140">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a32e4-140">This parameter is required.</span></span>

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

### <span data-ttu-id="a32e4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32e4-141">CommonParameters</span></span>
<span data-ttu-id="a32e4-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a32e4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32e4-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a32e4-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32e4-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a32e4-144">INPUTS</span></span>

### <span data-ttu-id="a32e4-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a32e4-145">None</span></span>
<span data-ttu-id="a32e4-146">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a32e4-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a32e4-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a32e4-147">OUTPUTS</span></span>

### <span data-ttu-id="a32e4-148">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a32e4-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="a32e4-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a32e4-149">NOTES</span></span>

## <span data-ttu-id="a32e4-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a32e4-150">RELATED LINKS</span></span>

[<span data-ttu-id="a32e4-151">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a32e4-151">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="a32e4-152">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a32e4-152">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="a32e4-153">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a32e4-153">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


