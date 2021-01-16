---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: c6af342183b7f1b2aa9bf7695ba8486ec193698a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259390"
---
# <span data-ttu-id="337c2-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="337c2-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="337c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="337c2-102">SYNOPSIS</span></span>
<span data-ttu-id="337c2-103">Cria um objeto de marca IP para uma interface de rede de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="337c2-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="337c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="337c2-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="337c2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="337c2-105">DESCRIPTION</span></span>
<span data-ttu-id="337c2-106">O cmdlet **New-AzVmssIpTagConfig** cria um objeto de configuração de marca IP para uma interface de rede de um conjunto de escala de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="337c2-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="337c2-107">Especifique a configuração deste cmdlet como o parâmetro *IPTag* do cmdlet New-AzVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="337c2-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="337c2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="337c2-108">EXAMPLES</span></span>

### <span data-ttu-id="337c2-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="337c2-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="337c2-110">Esse comando cria um objeto local de marca IP com o tipo ' FirstPartyUsage ' e a marca ' SQL ' e, em seguida, cria uma configuração de IP com essa marca de IP.</span><span class="sxs-lookup"><span data-stu-id="337c2-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="337c2-111">OS</span><span class="sxs-lookup"><span data-stu-id="337c2-111">PARAMETERS</span></span>

### <span data-ttu-id="337c2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="337c2-112">-DefaultProfile</span></span>
<span data-ttu-id="337c2-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="337c2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="337c2-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="337c2-114">-IpTagType</span></span>
<span data-ttu-id="337c2-115">Especifica um tipo de marca IP.</span><span class="sxs-lookup"><span data-stu-id="337c2-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="337c2-116">-Marca</span><span class="sxs-lookup"><span data-stu-id="337c2-116">-Tag</span></span>
<span data-ttu-id="337c2-117">Especifica um valor de marca IP.</span><span class="sxs-lookup"><span data-stu-id="337c2-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="337c2-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="337c2-118">-Confirm</span></span>
<span data-ttu-id="337c2-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="337c2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="337c2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="337c2-120">-WhatIf</span></span>
<span data-ttu-id="337c2-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="337c2-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="337c2-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="337c2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="337c2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="337c2-123">CommonParameters</span></span>
<span data-ttu-id="337c2-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="337c2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="337c2-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="337c2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="337c2-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="337c2-126">INPUTS</span></span>

### <span data-ttu-id="337c2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="337c2-127">System.String</span></span>

## <span data-ttu-id="337c2-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="337c2-128">OUTPUTS</span></span>

### <span data-ttu-id="337c2-129">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="337c2-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="337c2-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="337c2-130">NOTES</span></span>

## <span data-ttu-id="337c2-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="337c2-131">RELATED LINKS</span></span>
