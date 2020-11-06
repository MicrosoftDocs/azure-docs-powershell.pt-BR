---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: dc2e22acf8efd18a565c1ede7ff22aeb21679a47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429859"
---
# <span data-ttu-id="95f0c-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="95f0c-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="95f0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="95f0c-103">Remove a extensão chefe de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="95f0c-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95f0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95f0c-104">SYNTAX</span></span>

### <span data-ttu-id="95f0c-105">Linux</span><span class="sxs-lookup"><span data-stu-id="95f0c-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95f0c-106">Windows</span><span class="sxs-lookup"><span data-stu-id="95f0c-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95f0c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95f0c-107">DESCRIPTION</span></span>
<span data-ttu-id="95f0c-108">O cmdlet **Remove-AzureVMChefExtension** remove a extensão chefe de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="95f0c-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="95f0c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95f0c-109">EXAMPLES</span></span>

### <span data-ttu-id="95f0c-110">Exemplo 1: remover uma extensão chefe de um computador virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="95f0c-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="95f0c-111">Esse comando Remove uma extensão chefe de uma máquina virtual baseada em Windows nomeada WindowsVM001 que pertence ao grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="95f0c-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="95f0c-112">Exemplo 2: remover uma extensão chefe de um computador virtual Linux</span><span class="sxs-lookup"><span data-stu-id="95f0c-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="95f0c-113">Esse comando Remove uma extensão chefe de uma máquina virtual baseada em Linux nomeada LinuxVM001 que pertence ao grupo de recursos chamado ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="95f0c-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="95f0c-114">OS</span><span class="sxs-lookup"><span data-stu-id="95f0c-114">PARAMETERS</span></span>

### <span data-ttu-id="95f0c-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="95f0c-115">-Linux</span></span>
<span data-ttu-id="95f0c-116">Indica que esse cmdlet destina-se a um computador virtual Linux.</span><span class="sxs-lookup"><span data-stu-id="95f0c-116">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f0c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="95f0c-117">-Name</span></span>
<span data-ttu-id="95f0c-118">Especifica o nome da extensão chefe que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="95f0c-118">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95f0c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95f0c-119">-ResourceGroupName</span></span>
<span data-ttu-id="95f0c-120">Especifica o nome do grupo de recursos que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="95f0c-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="95f0c-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="95f0c-121">-VMName</span></span>
<span data-ttu-id="95f0c-122">Especifica o nome de uma máquina virtual para a qual esse cmdlet Remove a extensão chefe.</span><span class="sxs-lookup"><span data-stu-id="95f0c-122">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="95f0c-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="95f0c-123">-Windows</span></span>
<span data-ttu-id="95f0c-124">Indica que esse cmdlet se destina a um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="95f0c-124">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f0c-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="95f0c-125">-Confirm</span></span>
<span data-ttu-id="95f0c-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95f0c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95f0c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95f0c-127">-WhatIf</span></span>
<span data-ttu-id="95f0c-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="95f0c-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="95f0c-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="95f0c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95f0c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f0c-130">CommonParameters</span></span>
<span data-ttu-id="95f0c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95f0c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f0c-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95f0c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f0c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95f0c-133">INPUTS</span></span>

### <span data-ttu-id="95f0c-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="95f0c-134">None</span></span>
<span data-ttu-id="95f0c-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="95f0c-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95f0c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95f0c-136">OUTPUTS</span></span>

## <span data-ttu-id="95f0c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95f0c-137">NOTES</span></span>

## <span data-ttu-id="95f0c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95f0c-138">RELATED LINKS</span></span>

[<span data-ttu-id="95f0c-139">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="95f0c-139">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="95f0c-140">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="95f0c-140">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
