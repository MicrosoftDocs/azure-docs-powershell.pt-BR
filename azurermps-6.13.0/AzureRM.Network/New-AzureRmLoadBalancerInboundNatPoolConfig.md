---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 097377cd1ca4cb4be4fe62e2008f899c05c194fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440753"
---
# <span data-ttu-id="5caaa-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5caaa-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="5caaa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5caaa-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5caaa-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5caaa-103">SYNTAX</span></span>

### <span data-ttu-id="5caaa-104">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="5caaa-104">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5caaa-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5caaa-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5caaa-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5caaa-106">DESCRIPTION</span></span>

## <span data-ttu-id="5caaa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5caaa-107">EXAMPLES</span></span>

### <span data-ttu-id="5caaa-108">1: novo</span><span class="sxs-lookup"><span data-stu-id="5caaa-108">1: New</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzureRmLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="5caaa-109">OS</span><span class="sxs-lookup"><span data-stu-id="5caaa-109">PARAMETERS</span></span>

### <span data-ttu-id="5caaa-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="5caaa-110">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5caaa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5caaa-111">-DefaultProfile</span></span>
<span data-ttu-id="5caaa-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5caaa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5caaa-113">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="5caaa-113">-EnableFloatingIP</span></span>
<span data-ttu-id="5caaa-114">Configura o ponto de extremidade da máquina virtual para a funcionalidade de IP flutuante necessária para configurar um grupo de disponibilidade AlwaysOn do SQL.</span><span class="sxs-lookup"><span data-stu-id="5caaa-114">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="5caaa-115">Essa configuração é necessária ao usar os grupos de disponibilidade AlwaysOn do SQL no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5caaa-115">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="5caaa-116">Esta configuração não pode ser alterada depois que você cria o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5caaa-116">This setting can't be changed after you create the endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caaa-117">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="5caaa-117">-EnableTcpReset</span></span>
<span data-ttu-id="5caaa-118">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="5caaa-118">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="5caaa-119">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="5caaa-119">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caaa-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5caaa-120">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5caaa-121">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5caaa-121">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5caaa-122">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="5caaa-122">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5caaa-123">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="5caaa-123">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5caaa-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="5caaa-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="5caaa-125">O tempo limite para a conexão TCP ociosa.</span><span class="sxs-lookup"><span data-stu-id="5caaa-125">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="5caaa-126">O valor pode ser definido entre 4 e 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="5caaa-126">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="5caaa-127">O valor padrão é de 4 minutos.</span><span class="sxs-lookup"><span data-stu-id="5caaa-127">The default value is 4 minutes.</span></span> <span data-ttu-id="5caaa-128">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="5caaa-128">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5caaa-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="5caaa-129">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caaa-130">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="5caaa-130">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5caaa-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5caaa-131">-Confirm</span></span>
<span data-ttu-id="5caaa-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5caaa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5caaa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5caaa-133">-WhatIf</span></span>
<span data-ttu-id="5caaa-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5caaa-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5caaa-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5caaa-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5caaa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5caaa-136">CommonParameters</span></span>
<span data-ttu-id="5caaa-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5caaa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5caaa-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5caaa-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5caaa-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5caaa-139">INPUTS</span></span>

### <span data-ttu-id="5caaa-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5caaa-140">None</span></span>

## <span data-ttu-id="5caaa-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5caaa-141">OUTPUTS</span></span>

### <span data-ttu-id="5caaa-142">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="5caaa-142">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="5caaa-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5caaa-143">NOTES</span></span>

## <span data-ttu-id="5caaa-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5caaa-144">RELATED LINKS</span></span>
