---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
ms.openlocfilehash: 4e5e4a7dda9acac6d1da9fbce7e330b8c4bbb3ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602060"
---
# <span data-ttu-id="a1a49-101">Set-AzureRmVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="a1a49-101">Set-AzureRmVMBginfoExtension</span></span>

## <span data-ttu-id="a1a49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1a49-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a49-103">Adiciona a extensão do BGInfo a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1a49-103">Adds the BGInfo extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1a49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1a49-104">SYNTAX</span></span>

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1a49-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1a49-105">DESCRIPTION</span></span>
<span data-ttu-id="a1a49-106">O cmdlet **set-AzureRmVMBGInfoExtension** adiciona a extensão BGInfo a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1a49-106">The **Set-AzureRmVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="a1a49-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1a49-107">EXAMPLES</span></span>

### <span data-ttu-id="a1a49-108">Exemplo 1: adicionar a extensão do BGInfo para uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="a1a49-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -ResrouceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="a1a49-109">Esse comando adiciona a extensão BGInfo à máquina virtual chamada ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="a1a49-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="a1a49-110">O comando especifica o grupo de recursos e o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1a49-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="a1a49-111">O comando especifica o nome e a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="a1a49-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="a1a49-112">OS</span><span class="sxs-lookup"><span data-stu-id="a1a49-112">PARAMETERS</span></span>

### <span data-ttu-id="a1a49-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a49-113">-DefaultProfile</span></span>
<span data-ttu-id="a1a49-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a49-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1a49-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a1a49-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a1a49-116">Indica que esse cmdlet impede que o agente convidado do Azure atualize automaticamente a extensão para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="a1a49-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="a1a49-117">Por padrão, esse cmdlet permite que o agente de convidado atualize a extensão.</span><span class="sxs-lookup"><span data-stu-id="a1a49-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="a1a49-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="a1a49-118">-ForceRerun</span></span>
<span data-ttu-id="a1a49-119">Especifica que a extensão deve ser executada novamente com as mesmas configurações públicas ou protegidas.</span><span class="sxs-lookup"><span data-stu-id="a1a49-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="a1a49-120">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="a1a49-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="a1a49-121">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="a1a49-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="a1a49-122">-Local</span><span class="sxs-lookup"><span data-stu-id="a1a49-122">-Location</span></span>
<span data-ttu-id="a1a49-123">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1a49-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="a1a49-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1a49-124">-Name</span></span>
<span data-ttu-id="a1a49-125">Especifica o nome da extensão BGInfo que este cmdlet adiciona a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1a49-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="a1a49-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1a49-126">-ResourceGroupName</span></span>
<span data-ttu-id="a1a49-127">Especifica o nome do grupo de recursos da máquina virtual para a qual esse cmdlet adiciona uma extensão.</span><span class="sxs-lookup"><span data-stu-id="a1a49-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="a1a49-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a1a49-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="a1a49-129">Especifica a versão da extensão que esse cmdlet adiciona à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1a49-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="a1a49-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="a1a49-130">-VMName</span></span>
<span data-ttu-id="a1a49-131">Especifica o nome da máquina virtual para a qual esse cmdlet adiciona a extensão BGInfo.</span><span class="sxs-lookup"><span data-stu-id="a1a49-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="a1a49-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1a49-132">-Confirm</span></span>
<span data-ttu-id="a1a49-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1a49-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1a49-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1a49-134">-WhatIf</span></span>
<span data-ttu-id="a1a49-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1a49-135">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a1a49-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1a49-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1a49-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a49-137">CommonParameters</span></span>
<span data-ttu-id="a1a49-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1a49-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a49-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1a49-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a49-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1a49-140">INPUTS</span></span>

## <span data-ttu-id="a1a49-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1a49-141">OUTPUTS</span></span>

## <span data-ttu-id="a1a49-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1a49-142">NOTES</span></span>

## <span data-ttu-id="a1a49-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1a49-143">RELATED LINKS</span></span>

