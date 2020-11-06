---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: 1d7655a78ee2abe00b69d485c35b73cee91ee420
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602708"
---
# <span data-ttu-id="5ac23-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="5ac23-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="5ac23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ac23-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac23-103">Inicia uma atualização manual da instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="5ac23-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ac23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ac23-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ac23-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ac23-105">DESCRIPTION</span></span>
<span data-ttu-id="5ac23-106">O cmdlet Update-AzureRmVmssInstance inicia uma atualização manual da instância especificada do conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5ac23-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="5ac23-107">Isso é usado quando a política de atualização do conjunto de escala VMSS é definida como manual.</span><span class="sxs-lookup"><span data-stu-id="5ac23-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="5ac23-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ac23-108">EXAMPLES</span></span>

### <span data-ttu-id="5ac23-109">Exemplo 1: iniciar uma atualização da instância VMSS</span><span class="sxs-lookup"><span data-stu-id="5ac23-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="5ac23-110">Esse comando inicia uma atualização do VMSS chamado VMScaleSet001 que tem a ID de instância 0.</span><span class="sxs-lookup"><span data-stu-id="5ac23-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="5ac23-111">OS</span><span class="sxs-lookup"><span data-stu-id="5ac23-111">PARAMETERS</span></span>

### <span data-ttu-id="5ac23-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac23-112">-DefaultProfile</span></span>
<span data-ttu-id="5ac23-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac23-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ac23-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="5ac23-114">-InstanceId</span></span>
<span data-ttu-id="5ac23-115">Especifica, como uma matriz de cadeia de caracteres, a ID ou IDs da instância a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="5ac23-115">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac23-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac23-116">-ResourceGroupName</span></span>
<span data-ttu-id="5ac23-117">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="5ac23-117">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac23-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5ac23-118">-VMScaleSetName</span></span>
<span data-ttu-id="5ac23-119">Especifica o nome da instância VMSS que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="5ac23-119">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac23-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5ac23-120">-Confirm</span></span>
<span data-ttu-id="5ac23-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ac23-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ac23-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ac23-122">-WhatIf</span></span>
<span data-ttu-id="5ac23-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ac23-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5ac23-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ac23-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ac23-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac23-125">CommonParameters</span></span>
<span data-ttu-id="5ac23-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac23-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac23-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ac23-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac23-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ac23-128">INPUTS</span></span>

## <span data-ttu-id="5ac23-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ac23-129">OUTPUTS</span></span>

###  
<span data-ttu-id="5ac23-130">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="5ac23-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="5ac23-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ac23-131">NOTES</span></span>

## <span data-ttu-id="5ac23-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ac23-132">RELATED LINKS</span></span>

[<span data-ttu-id="5ac23-133">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5ac23-133">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


