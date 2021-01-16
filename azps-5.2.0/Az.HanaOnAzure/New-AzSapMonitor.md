---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: 95a9e996612827b355b141165231651e17c78f6d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259857"
---
# <span data-ttu-id="ce240-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="ce240-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="ce240-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce240-102">SYNOPSIS</span></span>
<span data-ttu-id="ce240-103">Cria um monitor SAP para a assinatura especificada, o grupo de recursos e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ce240-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="ce240-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce240-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ce240-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce240-105">DESCRIPTION</span></span>
<span data-ttu-id="ce240-106">Cria um monitor SAP para a assinatura especificada, o grupo de recursos e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ce240-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="ce240-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce240-107">EXAMPLES</span></span>

### <span data-ttu-id="ce240-108">Exemplo 1: novo monitor SAP</span><span class="sxs-lookup"><span data-stu-id="ce240-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="ce240-109">Esse comando cria um monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="ce240-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="ce240-110">OS</span><span class="sxs-lookup"><span data-stu-id="ce240-110">PARAMETERS</span></span>

### <span data-ttu-id="ce240-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce240-111">-AsJob</span></span>
<span data-ttu-id="ce240-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ce240-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ce240-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce240-113">-DefaultProfile</span></span>
<span data-ttu-id="ce240-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce240-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce240-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="ce240-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="ce240-116">O valor que indica se a análise deve ser enviada para a Microsoft</span><span class="sxs-lookup"><span data-stu-id="ce240-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="ce240-117">-Local</span><span class="sxs-lookup"><span data-stu-id="ce240-117">-Location</span></span>
<span data-ttu-id="ce240-118">A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="ce240-118">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="ce240-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="ce240-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="ce240-120">A ID do espaço de trabalho da análise de logs a ser usada para monitoramento</span><span class="sxs-lookup"><span data-stu-id="ce240-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce240-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="ce240-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="ce240-122">A ID do braço do espaço de trabalho de análise de log que é usada para monitorar</span><span class="sxs-lookup"><span data-stu-id="ce240-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce240-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="ce240-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="ce240-124">A chave compartilhada do espaço de trabalho análise de log que é usada para monitorar</span><span class="sxs-lookup"><span data-stu-id="ce240-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce240-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="ce240-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="ce240-126">A sub-rede na qual o monitor SAP será implantado.</span><span class="sxs-lookup"><span data-stu-id="ce240-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="ce240-127">Deve ser a mesma sub-rede do banco de dados HANA.</span><span class="sxs-lookup"><span data-stu-id="ce240-127">It should be the same subnet of HANA database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce240-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce240-128">-Name</span></span>
<span data-ttu-id="ce240-129">Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="ce240-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce240-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ce240-130">-NoWait</span></span>
<span data-ttu-id="ce240-131">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="ce240-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ce240-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce240-132">-ResourceGroupName</span></span>
<span data-ttu-id="ce240-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ce240-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="ce240-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce240-134">-SubscriptionId</span></span>
<span data-ttu-id="ce240-135">ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ce240-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ce240-136">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ce240-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce240-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="ce240-137">-Tag</span></span>
<span data-ttu-id="ce240-138">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="ce240-138">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce240-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ce240-139">-Confirm</span></span>
<span data-ttu-id="ce240-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce240-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce240-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce240-141">-WhatIf</span></span>
<span data-ttu-id="ce240-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ce240-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce240-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ce240-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce240-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce240-144">CommonParameters</span></span>
<span data-ttu-id="ce240-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce240-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce240-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce240-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce240-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce240-147">INPUTS</span></span>

## <span data-ttu-id="ce240-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce240-148">OUTPUTS</span></span>

### <span data-ttu-id="ce240-149">Microsoft. Azure. PowerShell. cmdlets. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="ce240-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="ce240-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce240-150">NOTES</span></span>

<span data-ttu-id="ce240-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ce240-151">ALIASES</span></span>

## <span data-ttu-id="ce240-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce240-152">RELATED LINKS</span></span>

