---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0335a063e810a94e6d557986e682ec4c777e5c1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776848"
---
# <span data-ttu-id="5360d-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5360d-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="5360d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5360d-102">SYNOPSIS</span></span>
<span data-ttu-id="5360d-103">Adiciona a extensão VMAccess a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5360d-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="5360d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5360d-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5360d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5360d-105">DESCRIPTION</span></span>
<span data-ttu-id="5360d-106">O cmdlet **set-AzVMAccessExtension** adiciona a extensão VMAccess virtual da máquina virtual do VMAccess (Virtual Machine Access) a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5360d-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="5360d-107">A extensão VMAccess pode ser usada para definir uma senha temporária e deve ser imediatamente alterada após o login na máquina.</span><span class="sxs-lookup"><span data-stu-id="5360d-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="5360d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5360d-108">EXAMPLES</span></span>

### <span data-ttu-id="5360d-109">Exemplo 1: adicionar uma extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="5360d-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="5360d-110">Esse comando adiciona uma extensão VMAccess para a máquina virtual nomeada VirtualMachine07 no ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5360d-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="5360d-111">O comando especifica o nome e a versão do manipulador de tipo para VMAccess.</span><span class="sxs-lookup"><span data-stu-id="5360d-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="5360d-112">OS</span><span class="sxs-lookup"><span data-stu-id="5360d-112">PARAMETERS</span></span>

### <span data-ttu-id="5360d-113">-Credential</span><span class="sxs-lookup"><span data-stu-id="5360d-113">-Credential</span></span>
<span data-ttu-id="5360d-114">Especifica o nome de usuário e a senha da máquina virtual como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="5360d-114">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="5360d-115">Para obter uma credencial, use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="5360d-115">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="5360d-116">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="5360d-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5360d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5360d-117">-DefaultProfile</span></span>
<span data-ttu-id="5360d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5360d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5360d-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5360d-119">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="5360d-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="5360d-120">-ForceRerun</span></span>
<span data-ttu-id="5360d-121">Indica que esse cmdlet força uma nova configuração da mesma extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="5360d-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="5360d-122">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="5360d-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="5360d-123">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="5360d-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="5360d-124">-Local</span><span class="sxs-lookup"><span data-stu-id="5360d-124">-Location</span></span>
<span data-ttu-id="5360d-125">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5360d-125">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="5360d-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="5360d-126">-Name</span></span>
<span data-ttu-id="5360d-127">Especifica o nome da extensão que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="5360d-127">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5360d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5360d-128">-ResourceGroupName</span></span>
<span data-ttu-id="5360d-129">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5360d-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5360d-130">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5360d-130">-TypeHandlerVersion</span></span>
<span data-ttu-id="5360d-131">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5360d-131">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="5360d-132">Para obter a versão, execute o cmdlet Get-AzVMExtensionImage com um valor de Microsoft. COMPUTE para o parâmetro *PublisherName* e VMAccessAgent para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="5360d-132">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5360d-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="5360d-133">-VMName</span></span>
<span data-ttu-id="5360d-134">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5360d-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5360d-135">Esse cmdlet adiciona VMAccess para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="5360d-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5360d-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5360d-136">-Confirm</span></span>
<span data-ttu-id="5360d-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5360d-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5360d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5360d-138">-WhatIf</span></span>
<span data-ttu-id="5360d-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5360d-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5360d-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5360d-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5360d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5360d-141">CommonParameters</span></span>
<span data-ttu-id="5360d-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5360d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5360d-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5360d-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5360d-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5360d-144">INPUTS</span></span>

### <span data-ttu-id="5360d-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5360d-145">None</span></span>
<span data-ttu-id="5360d-146">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5360d-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5360d-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5360d-147">OUTPUTS</span></span>

### <span data-ttu-id="5360d-148">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5360d-148">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5360d-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5360d-149">NOTES</span></span>

## <span data-ttu-id="5360d-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5360d-150">RELATED LINKS</span></span>

[<span data-ttu-id="5360d-151">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5360d-151">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="5360d-152">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5360d-152">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="5360d-153">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="5360d-153">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="5360d-154">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="5360d-154">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


