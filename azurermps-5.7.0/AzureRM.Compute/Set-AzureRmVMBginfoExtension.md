---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
ms.openlocfilehash: c52be698b216d206fe95ba5ea3aefc810f22fff2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427604"
---
# <span data-ttu-id="d2ce0-101">Set-AzureRmVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="d2ce0-101">Set-AzureRmVMBginfoExtension</span></span>

## <span data-ttu-id="d2ce0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ce0-103">Adiciona a extensão do BGInfo a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-103">Adds the BGInfo extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2ce0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2ce0-104">SYNTAX</span></span>

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2ce0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2ce0-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ce0-106">O cmdlet **set-AzureRmVMBGInfoExtension** adiciona a extensão BGInfo a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-106">The **Set-AzureRmVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="d2ce0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2ce0-107">EXAMPLES</span></span>

### <span data-ttu-id="d2ce0-108">Exemplo 1: adicionar a extensão do BGInfo a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d2ce0-108">Example 1: Add the BGInfo extension to a virtual machine</span></span>
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM"
```
<span data-ttu-id="d2ce0-109">Esse comando adiciona a extensão BGInfo a uma máquina virtual nomeada ContosoVM na ContosoRG do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-109">This command adds the BGInfo extension to a virtual machine named ContosoVM in the resource group ContosoRG.</span></span>

### <span data-ttu-id="d2ce0-110">Exemplo 2: adicionar uma versão específica da extensão do BGInfo a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d2ce0-110">Example 2: Add a specific version of BGInfo extension to a virtual machine</span></span>
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="d2ce0-111">Esse comando adiciona a extensão BGInfo à máquina virtual chamada ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-111">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="d2ce0-112">O comando especifica o grupo de recursos e o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-112">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="d2ce0-113">O comando especifica o nome e a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-113">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="d2ce0-114">OS</span><span class="sxs-lookup"><span data-stu-id="d2ce0-114">PARAMETERS</span></span>

### <span data-ttu-id="d2ce0-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d2ce0-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d2ce0-116">Indica que esse cmdlet impede que o agente convidado do Azure atualize automaticamente a extensão para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="d2ce0-117">Por padrão, esse cmdlet permite que o agente de convidado atualize a extensão.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="d2ce0-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="d2ce0-118">-ForceRerun</span></span>
<span data-ttu-id="d2ce0-119">Especifica que a extensão deve ser executada novamente com as mesmas configurações públicas ou protegidas.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="d2ce0-120">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="d2ce0-121">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="d2ce0-122">-Local</span><span class="sxs-lookup"><span data-stu-id="d2ce0-122">-Location</span></span>
<span data-ttu-id="d2ce0-123">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="d2ce0-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2ce0-124">-Name</span></span>
<span data-ttu-id="d2ce0-125">Especifica o nome da extensão BGInfo que este cmdlet adiciona a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="d2ce0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ce0-126">-ResourceGroupName</span></span>
<span data-ttu-id="d2ce0-127">Especifica o nome do grupo de recursos da máquina virtual para a qual esse cmdlet adiciona uma extensão.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="d2ce0-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d2ce0-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="d2ce0-129">Especifica a versão da extensão que esse cmdlet adiciona à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="d2ce0-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="d2ce0-130">-VMName</span></span>
<span data-ttu-id="d2ce0-131">Especifica o nome da máquina virtual para a qual esse cmdlet adiciona a extensão BGInfo.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="d2ce0-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2ce0-132">-Confirm</span></span>
<span data-ttu-id="d2ce0-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2ce0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ce0-134">-WhatIf</span></span>
<span data-ttu-id="d2ce0-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-135">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d2ce0-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2ce0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ce0-137">CommonParameters</span></span>
<span data-ttu-id="d2ce0-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ce0-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ce0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ce0-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2ce0-140">INPUTS</span></span>

### <span data-ttu-id="d2ce0-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d2ce0-141">None</span></span>
<span data-ttu-id="d2ce0-142">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d2ce0-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2ce0-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2ce0-143">OUTPUTS</span></span>

## <span data-ttu-id="d2ce0-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2ce0-144">NOTES</span></span>

## <span data-ttu-id="d2ce0-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2ce0-145">RELATED LINKS</span></span>

