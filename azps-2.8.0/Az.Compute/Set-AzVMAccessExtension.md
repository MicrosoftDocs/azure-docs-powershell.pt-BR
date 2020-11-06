---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: 8737801a798ac9d954d657db23f2500df028fa06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597231"
---
# <span data-ttu-id="21eeb-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="21eeb-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="21eeb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="21eeb-103">Adiciona a extensão VMAccess a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="21eeb-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="21eeb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21eeb-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21eeb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21eeb-105">DESCRIPTION</span></span>
<span data-ttu-id="21eeb-106">O cmdlet **set-AzVMAccessExtension** adiciona a extensão VMAccess virtual da máquina virtual do VMAccess (Virtual Machine Access) a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="21eeb-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="21eeb-107">A extensão VMAccess pode ser usada para definir uma senha temporária e deve ser imediatamente alterada após o login na máquina.</span><span class="sxs-lookup"><span data-stu-id="21eeb-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="21eeb-108">Isso não é compatível com os controladores de domínio do Windows.</span><span class="sxs-lookup"><span data-stu-id="21eeb-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="21eeb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21eeb-109">EXAMPLES</span></span>

### <span data-ttu-id="21eeb-110">Exemplo 1: adicionar uma extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="21eeb-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="21eeb-111">Esse comando adiciona uma extensão VMAccess para a máquina virtual nomeada VirtualMachine07 no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="21eeb-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>
<span data-ttu-id="21eeb-112">O comando especifica o nome e a versão do manipulador de tipo para VMAccess.</span><span class="sxs-lookup"><span data-stu-id="21eeb-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="21eeb-113">OS</span><span class="sxs-lookup"><span data-stu-id="21eeb-113">PARAMETERS</span></span>

### <span data-ttu-id="21eeb-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="21eeb-114">-Credential</span></span>
<span data-ttu-id="21eeb-115">Especifica o nome de usuário e a senha da máquina virtual como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="21eeb-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="21eeb-116">Se você digitar um nome diferente da conta de administrador local atual na VM, a extensão VMAccess adicionará uma conta de administrador local com esse nome e atribuirá sua senha especificada para essa conta.</span><span class="sxs-lookup"><span data-stu-id="21eeb-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="21eeb-117">Se houver uma conta de administrador local na sua VM, ela redefinirá a senha e, se a conta estiver desabilitada, a extensão VMAccess permitirá.</span><span class="sxs-lookup"><span data-stu-id="21eeb-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="21eeb-118">Para obter uma credencial, use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="21eeb-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="21eeb-119">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="21eeb-119">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="21eeb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21eeb-120">-DefaultProfile</span></span>
<span data-ttu-id="21eeb-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21eeb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21eeb-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="21eeb-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="21eeb-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="21eeb-123">-ForceRerun</span></span>
<span data-ttu-id="21eeb-124">Indica que esse cmdlet força uma nova configuração da mesma extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="21eeb-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="21eeb-125">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="21eeb-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="21eeb-126">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="21eeb-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="21eeb-127">-Local</span><span class="sxs-lookup"><span data-stu-id="21eeb-127">-Location</span></span>
<span data-ttu-id="21eeb-128">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="21eeb-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="21eeb-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="21eeb-129">-Name</span></span>
<span data-ttu-id="21eeb-130">Especifica o nome da extensão que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="21eeb-130">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="21eeb-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="21eeb-131">-NoWait</span></span>
<span data-ttu-id="21eeb-132">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="21eeb-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="21eeb-133">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="21eeb-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21eeb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21eeb-134">-ResourceGroupName</span></span>
<span data-ttu-id="21eeb-135">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="21eeb-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="21eeb-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="21eeb-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="21eeb-137">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="21eeb-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="21eeb-138">Para obter a versão, execute o cmdlet Get-AzVMExtensionImage com um valor de Microsoft. COMPUTE para o parâmetro *PublisherName* e VMAccessAgent para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="21eeb-138">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="21eeb-139">O typeHandlerVersion deve ser 2,0 ou posterior, pois a versão 1 foi preterida.</span><span class="sxs-lookup"><span data-stu-id="21eeb-139">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="21eeb-140">-VMName</span><span class="sxs-lookup"><span data-stu-id="21eeb-140">-VMName</span></span>
<span data-ttu-id="21eeb-141">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="21eeb-141">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="21eeb-142">Esse cmdlet adiciona VMAccess para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="21eeb-142">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="21eeb-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="21eeb-143">-Confirm</span></span>
<span data-ttu-id="21eeb-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21eeb-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21eeb-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21eeb-145">-WhatIf</span></span>
<span data-ttu-id="21eeb-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21eeb-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21eeb-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21eeb-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21eeb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21eeb-148">CommonParameters</span></span>
<span data-ttu-id="21eeb-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21eeb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21eeb-150">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21eeb-150">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21eeb-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21eeb-151">INPUTS</span></span>

### <span data-ttu-id="21eeb-152">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="21eeb-152">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="21eeb-153">System. String</span><span class="sxs-lookup"><span data-stu-id="21eeb-153">System.String</span></span>

### <span data-ttu-id="21eeb-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="21eeb-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="21eeb-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21eeb-155">OUTPUTS</span></span>

### <span data-ttu-id="21eeb-156">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="21eeb-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="21eeb-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21eeb-157">NOTES</span></span>

## <span data-ttu-id="21eeb-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21eeb-158">RELATED LINKS</span></span>

[<span data-ttu-id="21eeb-159">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="21eeb-159">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="21eeb-160">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="21eeb-160">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="21eeb-161">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="21eeb-161">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="21eeb-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="21eeb-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


