---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: 241b8938be77d9074000a116f82d8b2bcdffc5b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892536"
---
# <span data-ttu-id="0087c-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="0087c-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="0087c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0087c-102">SYNOPSIS</span></span>
<span data-ttu-id="0087c-103">Cria um objeto IP Tag para uma interface de rede de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="0087c-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="0087c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0087c-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0087c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0087c-105">DESCRIPTION</span></span>
<span data-ttu-id="0087c-106">O cmdlet **New-AzVmssIpTagConfig** cria um objeto de configuração de MARCA IP para uma interface de rede de um Conjunto de Escala de Máquina Virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="0087c-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="0087c-107">Especifique a configuração deste cmdlet como o parâmetro *IPTag* do cmdlet New-AzVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="0087c-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="0087c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0087c-108">EXAMPLES</span></span>

### <span data-ttu-id="0087c-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0087c-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="0087c-110">Este comando cria um objeto local de Marca IP com o tipo 'FirstPartyUsage' e a marca 'Sql' e cria uma configuração IP com essa marca IP.</span><span class="sxs-lookup"><span data-stu-id="0087c-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="0087c-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0087c-111">PARAMETERS</span></span>

### <span data-ttu-id="0087c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0087c-112">-DefaultProfile</span></span>
<span data-ttu-id="0087c-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0087c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0087c-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="0087c-114">-IpTagType</span></span>
<span data-ttu-id="0087c-115">Especifica um tipo de marca IP.</span><span class="sxs-lookup"><span data-stu-id="0087c-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="0087c-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="0087c-116">-Tag</span></span>
<span data-ttu-id="0087c-117">Especifica um valor de marca IP.</span><span class="sxs-lookup"><span data-stu-id="0087c-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="0087c-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0087c-118">-Confirm</span></span>
<span data-ttu-id="0087c-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0087c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0087c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0087c-120">-WhatIf</span></span>
<span data-ttu-id="0087c-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0087c-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0087c-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0087c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0087c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0087c-123">CommonParameters</span></span>
<span data-ttu-id="0087c-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0087c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0087c-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0087c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0087c-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0087c-126">INPUTS</span></span>

### <span data-ttu-id="0087c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0087c-127">System.String</span></span>

## <span data-ttu-id="0087c-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0087c-128">OUTPUTS</span></span>

### <span data-ttu-id="0087c-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="0087c-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="0087c-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="0087c-130">NOTES</span></span>

## <span data-ttu-id="0087c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0087c-131">RELATED LINKS</span></span>
