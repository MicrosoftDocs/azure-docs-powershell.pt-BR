---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 069b98f585d606ade255cfecd223be4a074d8316
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785949"
---
# <span data-ttu-id="f0d2e-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f0d2e-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="f0d2e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d2e-103">Adiciona a extensão VMAccess a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0d2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0d2e-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0d2e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0d2e-105">DESCRIPTION</span></span>
<span data-ttu-id="f0d2e-106">O cmdlet **set-AzureRmVMAccessExtension** adiciona a extensão VMAccess virtual da máquina virtual do VMAccess (Virtual Machine Access) a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="f0d2e-107">A extensão VMAccess pode ser usada para definir uma senha temporária e deve ser imediatamente alterada após o login na máquina.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="f0d2e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0d2e-108">EXAMPLES</span></span>

### <span data-ttu-id="f0d2e-109">Exemplo 1: adicionar uma extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="f0d2e-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="f0d2e-110">Esse comando adiciona uma extensão VMAccess para a máquina virtual nomeada VirtualMachine07 no ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="f0d2e-111">O comando especifica o nome e a versão do manipulador de tipo para VMAccess.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="f0d2e-112">OS</span><span class="sxs-lookup"><span data-stu-id="f0d2e-112">PARAMETERS</span></span>

### <span data-ttu-id="f0d2e-113">-Credential</span><span class="sxs-lookup"><span data-stu-id="f0d2e-113">-Credential</span></span>
<span data-ttu-id="f0d2e-114">Especifica o nome de usuário e a senha da máquina virtual como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="f0d2e-114">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="f0d2e-115">Para obter uma credencial, use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-115">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="f0d2e-116">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="f0d2e-116">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="f0d2e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d2e-117">-DefaultProfile</span></span>
<span data-ttu-id="f0d2e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0d2e-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f0d2e-119">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="f0d2e-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="f0d2e-120">-ForceRerun</span></span>
<span data-ttu-id="f0d2e-121">Indica que esse cmdlet força uma nova configuração da mesma extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="f0d2e-122">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="f0d2e-123">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="f0d2e-124">-Local</span><span class="sxs-lookup"><span data-stu-id="f0d2e-124">-Location</span></span>
<span data-ttu-id="f0d2e-125">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-125">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="f0d2e-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0d2e-126">-Name</span></span>
<span data-ttu-id="f0d2e-127">Especifica o nome da extensão que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-127">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f0d2e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d2e-128">-ResourceGroupName</span></span>
<span data-ttu-id="f0d2e-129">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f0d2e-130">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f0d2e-130">-TypeHandlerVersion</span></span>
<span data-ttu-id="f0d2e-131">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-131">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="f0d2e-132">Para obter a versão, execute o cmdlet Get-AzureRmVMExtensionImage com um valor de Microsoft. COMPUTE para o parâmetro *PublisherName* e VMAccessAgent para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="f0d2e-132">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="f0d2e-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="f0d2e-133">-VMName</span></span>
<span data-ttu-id="f0d2e-134">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f0d2e-135">Esse cmdlet adiciona VMAccess para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f0d2e-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f0d2e-136">-Confirm</span></span>
<span data-ttu-id="f0d2e-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0d2e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0d2e-138">-WhatIf</span></span>
<span data-ttu-id="f0d2e-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f0d2e-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0d2e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d2e-141">CommonParameters</span></span>
<span data-ttu-id="f0d2e-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d2e-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d2e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d2e-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0d2e-144">INPUTS</span></span>

### <span data-ttu-id="f0d2e-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f0d2e-145">None</span></span>
<span data-ttu-id="f0d2e-146">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f0d2e-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0d2e-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0d2e-147">OUTPUTS</span></span>

### <span data-ttu-id="f0d2e-148">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f0d2e-148">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f0d2e-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0d2e-149">NOTES</span></span>

## <span data-ttu-id="f0d2e-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0d2e-150">RELATED LINKS</span></span>

[<span data-ttu-id="f0d2e-151">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f0d2e-151">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="f0d2e-152">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f0d2e-152">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="f0d2e-153">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f0d2e-153">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="f0d2e-154">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="f0d2e-154">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


