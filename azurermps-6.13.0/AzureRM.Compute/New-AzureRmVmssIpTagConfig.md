---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
ms.openlocfilehash: a77680921eeef0a678cbd83d04bef9a51cf35cb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426415"
---
# <span data-ttu-id="b53f9-101">New-AzureRmVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="b53f9-101">New-AzureRmVmssIpTagConfig</span></span>

## <span data-ttu-id="b53f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b53f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b53f9-103">Cria um objeto de marca IP para uma interface de rede de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="b53f9-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b53f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b53f9-104">SYNTAX</span></span>

```
New-AzureRmVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b53f9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b53f9-105">DESCRIPTION</span></span>
<span data-ttu-id="b53f9-106">O cmdlet **New-AzureRmVmssIpTagConfig** cria um objeto de configuração de marca IP para uma interface de rede de um conjunto de escala de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b53f9-106">The **New-AzureRmVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="b53f9-107">Especifique a configuração deste cmdlet como o parâmetro *IPTag* do cmdlet New-AzureRmVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="b53f9-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzureRmVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="b53f9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b53f9-108">EXAMPLES</span></span>

### <span data-ttu-id="b53f9-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b53f9-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzureRmVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzureRmVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="b53f9-110">Esse comando cria um objeto local de marca IP com o tipo ' FirstPartyUsage ' e a marca ' SQL ' e, em seguida, cria uma configuração de IP com essa marca de IP.</span><span class="sxs-lookup"><span data-stu-id="b53f9-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="b53f9-111">OS</span><span class="sxs-lookup"><span data-stu-id="b53f9-111">PARAMETERS</span></span>

### <span data-ttu-id="b53f9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b53f9-112">-DefaultProfile</span></span>
<span data-ttu-id="b53f9-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b53f9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b53f9-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="b53f9-114">-IpTagType</span></span>
<span data-ttu-id="b53f9-115">Especifica um tipo de marca IP.</span><span class="sxs-lookup"><span data-stu-id="b53f9-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="b53f9-116">-Marca</span><span class="sxs-lookup"><span data-stu-id="b53f9-116">-Tag</span></span>
<span data-ttu-id="b53f9-117">Especifica um valor de marca IP.</span><span class="sxs-lookup"><span data-stu-id="b53f9-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="b53f9-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b53f9-118">-Confirm</span></span>
<span data-ttu-id="b53f9-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b53f9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b53f9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b53f9-120">-WhatIf</span></span>
<span data-ttu-id="b53f9-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b53f9-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b53f9-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b53f9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b53f9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b53f9-123">CommonParameters</span></span>
<span data-ttu-id="b53f9-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b53f9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b53f9-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b53f9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b53f9-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b53f9-126">INPUTS</span></span>

### <span data-ttu-id="b53f9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b53f9-127">System.String</span></span>

## <span data-ttu-id="b53f9-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b53f9-128">OUTPUTS</span></span>

### <span data-ttu-id="b53f9-129">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="b53f9-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="b53f9-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b53f9-130">NOTES</span></span>

## <span data-ttu-id="b53f9-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b53f9-131">RELATED LINKS</span></span>
