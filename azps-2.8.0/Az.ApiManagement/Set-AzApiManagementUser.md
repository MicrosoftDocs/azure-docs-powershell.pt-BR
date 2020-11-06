---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: ccd19f0390957466f9fb799d3655aa8bb1d02d68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597919"
---
# <span data-ttu-id="51cb6-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="51cb6-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="51cb6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="51cb6-103">Define detalhes do usuário.</span><span class="sxs-lookup"><span data-stu-id="51cb6-103">Sets user details.</span></span>

## <span data-ttu-id="51cb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51cb6-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51cb6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51cb6-105">DESCRIPTION</span></span>
<span data-ttu-id="51cb6-106">O cmdlet **set-AzApiManagementUser** define detalhes do usuário.</span><span class="sxs-lookup"><span data-stu-id="51cb6-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="51cb6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51cb6-107">EXAMPLES</span></span>

### <span data-ttu-id="51cb6-108">Exemplo 1: alterar a senha de um usuário, o endereço de email e o estado</span><span class="sxs-lookup"><span data-stu-id="51cb6-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="51cb6-109">Esse comando define uma nova senha de usuário e um endereço de email e bloqueia o usuário.</span><span class="sxs-lookup"><span data-stu-id="51cb6-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="51cb6-110">OS</span><span class="sxs-lookup"><span data-stu-id="51cb6-110">PARAMETERS</span></span>

### <span data-ttu-id="51cb6-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="51cb6-111">-Context</span></span>
<span data-ttu-id="51cb6-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="51cb6-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="51cb6-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="51cb6-113">This parameter is required.</span></span>

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

### <span data-ttu-id="51cb6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51cb6-114">-DefaultProfile</span></span>
<span data-ttu-id="51cb6-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51cb6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51cb6-116">-Email</span><span class="sxs-lookup"><span data-stu-id="51cb6-116">-Email</span></span>
<span data-ttu-id="51cb6-117">Especifica o endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="51cb6-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="51cb6-118">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="51cb6-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="51cb6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="51cb6-119">-FirstName</span></span>
<span data-ttu-id="51cb6-120">Especifica o primeiro nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="51cb6-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="51cb6-121">Esse parâmetro deve ter de 1 a 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="51cb6-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="51cb6-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="51cb6-122">-LastName</span></span>
<span data-ttu-id="51cb6-123">Especifica o último nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="51cb6-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="51cb6-124">Esse parâmetro deve ter entre 1 e 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="51cb6-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="51cb6-125">-Nota</span><span class="sxs-lookup"><span data-stu-id="51cb6-125">-Note</span></span>
<span data-ttu-id="51cb6-126">Especifica uma observação sobre o usuário.</span><span class="sxs-lookup"><span data-stu-id="51cb6-126">Specifies a note about the user.</span></span>
<span data-ttu-id="51cb6-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="51cb6-127">This parameter is optional.</span></span>
<span data-ttu-id="51cb6-128">O valor padrão desse parâmetro é $null.</span><span class="sxs-lookup"><span data-stu-id="51cb6-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="51cb6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51cb6-129">-PassThru</span></span>
<span data-ttu-id="51cb6-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="51cb6-130">passthru</span></span>

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

### <span data-ttu-id="51cb6-131">-Senha</span><span class="sxs-lookup"><span data-stu-id="51cb6-131">-Password</span></span>
<span data-ttu-id="51cb6-132">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="51cb6-132">Specifies the user password.</span></span>
<span data-ttu-id="51cb6-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="51cb6-133">This parameter is optional.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51cb6-134">-Estado</span><span class="sxs-lookup"><span data-stu-id="51cb6-134">-State</span></span>
<span data-ttu-id="51cb6-135">Especifica o estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="51cb6-135">Specifies the user state.</span></span>
<span data-ttu-id="51cb6-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="51cb6-136">This parameter is optional.</span></span>
<span data-ttu-id="51cb6-137">O valor padrão é ativo.</span><span class="sxs-lookup"><span data-stu-id="51cb6-137">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51cb6-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="51cb6-138">-UserId</span></span>
<span data-ttu-id="51cb6-139">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="51cb6-139">Specifies the user ID.</span></span>
<span data-ttu-id="51cb6-140">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="51cb6-140">This parameter is required.</span></span>

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

### <span data-ttu-id="51cb6-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="51cb6-141">-Confirm</span></span>
<span data-ttu-id="51cb6-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51cb6-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cb6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51cb6-143">-WhatIf</span></span>
<span data-ttu-id="51cb6-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51cb6-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51cb6-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51cb6-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cb6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51cb6-146">CommonParameters</span></span>
<span data-ttu-id="51cb6-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51cb6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51cb6-148">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51cb6-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51cb6-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51cb6-149">INPUTS</span></span>

### <span data-ttu-id="51cb6-150">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="51cb6-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="51cb6-151">System. String</span><span class="sxs-lookup"><span data-stu-id="51cb6-151">System.String</span></span>

### <span data-ttu-id="51cb6-152">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="51cb6-152">System.Security.SecureString</span></span>

### <span data-ttu-id="51cb6-153">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="51cb6-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="51cb6-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="51cb6-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="51cb6-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51cb6-155">OUTPUTS</span></span>

### <span data-ttu-id="51cb6-156">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="51cb6-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="51cb6-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51cb6-157">NOTES</span></span>

## <span data-ttu-id="51cb6-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51cb6-158">RELATED LINKS</span></span>

[<span data-ttu-id="51cb6-159">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="51cb6-159">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="51cb6-160">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="51cb6-160">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="51cb6-161">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="51cb6-161">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)


