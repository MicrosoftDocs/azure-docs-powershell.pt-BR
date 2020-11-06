---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: 0a2d3ce354a5039db21fdd336f6f2d64efdb56fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440808"
---
# <span data-ttu-id="9975b-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9975b-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="9975b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9975b-102">SYNOPSIS</span></span>
<span data-ttu-id="9975b-103">Adiciona a extensão VMAccess a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9975b-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9975b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9975b-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9975b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9975b-105">DESCRIPTION</span></span>
<span data-ttu-id="9975b-106">O cmdlet **set-AzureRmVMAccessExtension** adiciona a extensão VMAccess virtual da máquina virtual do VMAccess (Virtual Machine Access) a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9975b-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="9975b-107">A extensão VMAccess pode ser usada para definir uma senha temporária e deve ser imediatamente alterada após o login na máquina.</span><span class="sxs-lookup"><span data-stu-id="9975b-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="9975b-108">Isso não é compatível com os controladores de domínio do Windows.</span><span class="sxs-lookup"><span data-stu-id="9975b-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="9975b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9975b-109">EXAMPLES</span></span>

### <span data-ttu-id="9975b-110">Exemplo 1: adicionar uma extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="9975b-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.4" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="9975b-111">Esse comando adiciona uma extensão VMAccess para a máquina virtual nomeada VirtualMachine07 no ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9975b-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="9975b-112">O comando especifica o nome e a versão do manipulador de tipo para VMAccess.</span><span class="sxs-lookup"><span data-stu-id="9975b-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="9975b-113">OS</span><span class="sxs-lookup"><span data-stu-id="9975b-113">PARAMETERS</span></span>

### <span data-ttu-id="9975b-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="9975b-114">-Credential</span></span>
<span data-ttu-id="9975b-115">Especifica o nome de usuário e a senha da máquina virtual como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="9975b-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="9975b-116">Se você digitar um nome diferente da conta de administrador local atual na VM, a extensão VMAccess adicionará uma conta de administrador local com esse nome e atribuirá sua senha especificada para essa conta.</span><span class="sxs-lookup"><span data-stu-id="9975b-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="9975b-117">Se houver uma conta de administrador local na sua VM, ela redefinirá a senha e, se a conta estiver desabilitada, a extensão VMAccess permitirá.</span><span class="sxs-lookup"><span data-stu-id="9975b-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="9975b-118">Para obter uma credencial, use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="9975b-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="9975b-119">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="9975b-119">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9975b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9975b-120">-DefaultProfile</span></span>
<span data-ttu-id="9975b-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9975b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9975b-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9975b-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="9975b-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="9975b-123">-ForceRerun</span></span>
<span data-ttu-id="9975b-124">Indica que esse cmdlet força uma nova configuração da mesma extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="9975b-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="9975b-125">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="9975b-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="9975b-126">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="9975b-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="9975b-127">-Local</span><span class="sxs-lookup"><span data-stu-id="9975b-127">-Location</span></span>
<span data-ttu-id="9975b-128">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9975b-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="9975b-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="9975b-129">-Name</span></span>
<span data-ttu-id="9975b-130">Especifica o nome da extensão que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="9975b-130">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9975b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9975b-131">-ResourceGroupName</span></span>
<span data-ttu-id="9975b-132">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9975b-132">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9975b-133">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9975b-133">-TypeHandlerVersion</span></span>
<span data-ttu-id="9975b-134">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9975b-134">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="9975b-135">Para obter a versão, execute o cmdlet Get-AzureRmVMExtensionImage com um valor de Microsoft. COMPUTE para o parâmetro *PublisherName* e VMAccessAgent para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="9975b-135">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="9975b-136">O typeHandlerVersion deve ser 2,0 ou posterior, pois a versão 1 foi preterida.</span><span class="sxs-lookup"><span data-stu-id="9975b-136">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9975b-137">-VMName</span><span class="sxs-lookup"><span data-stu-id="9975b-137">-VMName</span></span>
<span data-ttu-id="9975b-138">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9975b-138">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9975b-139">Esse cmdlet adiciona VMAccess para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9975b-139">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9975b-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9975b-140">-Confirm</span></span>
<span data-ttu-id="9975b-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9975b-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9975b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9975b-142">-WhatIf</span></span>
<span data-ttu-id="9975b-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9975b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9975b-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9975b-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9975b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9975b-145">CommonParameters</span></span>
<span data-ttu-id="9975b-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9975b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9975b-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9975b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9975b-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9975b-148">INPUTS</span></span>

### <span data-ttu-id="9975b-149">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="9975b-149">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="9975b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="9975b-150">System.String</span></span>

### <span data-ttu-id="9975b-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9975b-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9975b-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9975b-152">OUTPUTS</span></span>

### <span data-ttu-id="9975b-153">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9975b-153">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9975b-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9975b-154">NOTES</span></span>

## <span data-ttu-id="9975b-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9975b-155">RELATED LINKS</span></span>

[<span data-ttu-id="9975b-156">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9975b-156">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="9975b-157">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9975b-157">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="9975b-158">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="9975b-158">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="9975b-159">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="9975b-159">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


