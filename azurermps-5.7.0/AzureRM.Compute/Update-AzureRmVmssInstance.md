---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: 75b8190c34d5335904d40d386cabc76e8cbf0b0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426758"
---
# <span data-ttu-id="01f05-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="01f05-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="01f05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01f05-102">SYNOPSIS</span></span>
<span data-ttu-id="01f05-103">Inicia uma atualização manual da instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="01f05-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01f05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01f05-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01f05-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01f05-105">DESCRIPTION</span></span>
<span data-ttu-id="01f05-106">O cmdlet Update-AzureRmVmssInstance inicia uma atualização manual da instância especificada do conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="01f05-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="01f05-107">Isso é usado quando a política de atualização do conjunto de escala VMSS é definida como manual.</span><span class="sxs-lookup"><span data-stu-id="01f05-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="01f05-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01f05-108">EXAMPLES</span></span>

### <span data-ttu-id="01f05-109">Exemplo 1: iniciar uma atualização da instância VMSS</span><span class="sxs-lookup"><span data-stu-id="01f05-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="01f05-110">Esse comando inicia uma atualização do VMSS chamado VMScaleSet001 que tem a ID de instância 0.</span><span class="sxs-lookup"><span data-stu-id="01f05-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="01f05-111">OS</span><span class="sxs-lookup"><span data-stu-id="01f05-111">PARAMETERS</span></span>

### <span data-ttu-id="01f05-112">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="01f05-112">-InstanceId</span></span>
<span data-ttu-id="01f05-113">Especifica, como uma matriz de cadeia de caracteres, a ID ou IDs da instância a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="01f05-113">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01f05-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01f05-114">-ResourceGroupName</span></span>
<span data-ttu-id="01f05-115">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="01f05-115">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01f05-116">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="01f05-116">-VMScaleSetName</span></span>
<span data-ttu-id="01f05-117">Especifica o nome da instância VMSS que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="01f05-117">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01f05-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="01f05-118">-Confirm</span></span>
<span data-ttu-id="01f05-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01f05-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01f05-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01f05-120">-WhatIf</span></span>
<span data-ttu-id="01f05-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="01f05-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="01f05-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01f05-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01f05-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f05-123">CommonParameters</span></span>
<span data-ttu-id="01f05-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01f05-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f05-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01f05-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f05-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01f05-126">INPUTS</span></span>

### <span data-ttu-id="01f05-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="01f05-127">None</span></span>
<span data-ttu-id="01f05-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="01f05-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01f05-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01f05-129">OUTPUTS</span></span>

###  
<span data-ttu-id="01f05-130">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="01f05-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="01f05-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01f05-131">NOTES</span></span>

## <span data-ttu-id="01f05-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01f05-132">RELATED LINKS</span></span>

[<span data-ttu-id="01f05-133">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="01f05-133">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


