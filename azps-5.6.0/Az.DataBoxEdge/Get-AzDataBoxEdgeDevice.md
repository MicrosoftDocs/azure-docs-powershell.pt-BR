---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: f02cda5fe04ed72a5e6defd382c372b40c9c039b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891393"
---
# <span data-ttu-id="ac8ab-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ac8ab-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="ac8ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac8ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ac8ab-103">Obtém as informações sobre dispositivos de Borda da Caixa de Dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ac8ab-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="ac8ab-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ac8ab-104">SYNTAX</span></span>

### <span data-ttu-id="ac8ab-105">ListByParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ac8ab-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac8ab-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac8ab-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac8ab-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac8ab-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac8ab-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac8ab-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac8ab-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac8ab-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac8ab-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac8ab-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac8ab-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac8ab-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac8ab-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac8ab-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac8ab-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac8ab-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac8ab-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac8ab-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac8ab-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac8ab-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac8ab-116">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ac8ab-116">DESCRIPTION</span></span>
<span data-ttu-id="ac8ab-117">O cmdlet **Get-AzDataBoxEdgeDevice** obtém as informações sobre os Dispositivos de Borda da Caixa de Dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ac8ab-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="ac8ab-118">Você pode especificar o Nome do dispositivo juntamente com o Nome do Grupo de Recursos para obter as informações em um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="ac8ab-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="ac8ab-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac8ab-119">EXAMPLES</span></span>

### <span data-ttu-id="ac8ab-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ac8ab-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="ac8ab-121">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ac8ab-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="ac8ab-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ac8ab-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="ac8ab-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ac8ab-123">PARAMETERS</span></span>

### <span data-ttu-id="ac8ab-124">-Alert</span><span class="sxs-lookup"><span data-stu-id="ac8ab-124">-Alert</span></span>
<span data-ttu-id="ac8ab-125">Buscar os alertas no dispositivo de borda/gateway da caixa de dados</span><span class="sxs-lookup"><span data-stu-id="ac8ab-125">Fetch the alerts on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAlertByResourceIdParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8ab-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac8ab-126">-DefaultProfile</span></span>
<span data-ttu-id="ac8ab-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac8ab-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac8ab-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="ac8ab-128">-ExtendedInfo</span></span>
<span data-ttu-id="ac8ab-129">Obtém informações adicionais para o dispositivo de Gateway de Caixa de Dados/Borda da Caixa de Dados especificado</span><span class="sxs-lookup"><span data-stu-id="ac8ab-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetExtendedInfoByResourceIdParameterSet, GetExtendedInfoParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8ab-130">-Name</span><span class="sxs-lookup"><span data-stu-id="ac8ab-130">-Name</span></span>
<span data-ttu-id="ac8ab-131">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ac8ab-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8ab-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="ac8ab-132">-NetworkSetting</span></span>
<span data-ttu-id="ac8ab-133">Obtém as configurações de rede do dispositivo de Gateway de Caixa de Dados/Caixa de Dados especificado</span><span class="sxs-lookup"><span data-stu-id="ac8ab-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNetworkSettingByResourceIdParameterSet, GetNetworkSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8ab-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac8ab-134">-ResourceGroupName</span></span>
<span data-ttu-id="ac8ab-135">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ac8ab-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8ab-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac8ab-136">-ResourceId</span></span>
<span data-ttu-id="ac8ab-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac8ab-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet, GetExtendedInfoByResourceIdParameterSet, GetNetworkSettingByResourceIdParameterSet, GetSummaryUpdateByResourceIdParameterSet, GetAlertByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8ab-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="ac8ab-138">-UpdateSummary</span></span>
<span data-ttu-id="ac8ab-139">Obtém informações sobre a disponibilidade de atualizações com base na última verificação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac8ab-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="ac8ab-140">Ele também obtém informações sobre quaisquer trabalhos de download ou instalação em andamento no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac8ab-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetSummaryUpdateByResourceIdParameterSet, GetSummaryUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8ab-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac8ab-141">CommonParameters</span></span>
<span data-ttu-id="ac8ab-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac8ab-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac8ab-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac8ab-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac8ab-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac8ab-144">INPUTS</span></span>

### <span data-ttu-id="ac8ab-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac8ab-145">None</span></span>

## <span data-ttu-id="ac8ab-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ac8ab-146">OUTPUTS</span></span>

### <span data-ttu-id="ac8ab-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ac8ab-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="ac8ab-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="ac8ab-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="ac8ab-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="ac8ab-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="ac8ab-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="ac8ab-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="ac8ab-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="ac8ab-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="ac8ab-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="ac8ab-152">NOTES</span></span>

## <span data-ttu-id="ac8ab-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac8ab-153">RELATED LINKS</span></span>
