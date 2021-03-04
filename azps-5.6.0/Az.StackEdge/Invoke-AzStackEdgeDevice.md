---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: 63d364ac12d47f5bb15e877e5076550a0cbd3f16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892311"
---
# <span data-ttu-id="c4fe3-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c4fe3-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="c4fe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="c4fe3-103">Invoca ações específicas no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4fe3-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="c4fe3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c4fe3-104">SYNTAX</span></span>

### <span data-ttu-id="c4fe3-105">InvokeScanForUpdateParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c4fe3-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4fe3-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4fe3-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4fe3-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4fe3-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4fe3-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4fe3-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4fe3-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4fe3-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4fe3-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4fe3-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4fe3-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4fe3-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4fe3-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4fe3-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4fe3-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4fe3-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4fe3-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c4fe3-114">DESCRIPTION</span></span>
<span data-ttu-id="c4fe3-115">O cmdlet **Invoke-AzStackEdgeDevice** invoca ações para verificar, baixar e instalar as atualizações no dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="c4fe3-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="c4fe3-116">Uma verificação automática é executado no dispositivo diariamente, você pode acionar a verificação explicitamente executando este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4fe3-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="c4fe3-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4fe3-117">EXAMPLES</span></span>

### <span data-ttu-id="c4fe3-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c4fe3-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="c4fe3-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c4fe3-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="c4fe3-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c4fe3-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="c4fe3-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c4fe3-121">PARAMETERS</span></span>

### <span data-ttu-id="c4fe3-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4fe3-122">-AsJob</span></span>
<span data-ttu-id="c4fe3-123">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c4fe3-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4fe3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4fe3-124">-DefaultProfile</span></span>
<span data-ttu-id="c4fe3-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4fe3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4fe3-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c4fe3-126">-DeviceObject</span></span>
<span data-ttu-id="c4fe3-127">Forneça o objeto de dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="c4fe3-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fe3-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="c4fe3-128">-FetchUpdate</span></span>
<span data-ttu-id="c4fe3-129">Baixa as atualizações em um dispositivo de borda/gateway stack</span><span class="sxs-lookup"><span data-stu-id="c4fe3-129">Downloads the updates on a Stack edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeFetchUpdateParameterSet, InvokeFetchUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fe3-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="c4fe3-130">-InstallUpdate</span></span>
<span data-ttu-id="c4fe3-131">Instala as atualizações no dispositivo stack edge/gateway</span><span class="sxs-lookup"><span data-stu-id="c4fe3-131">Installs the updates on the Stack edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeInstallUpdatesByResourceIdParameterSet, InvokeInstallUpdateParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fe3-132">-Name</span><span class="sxs-lookup"><span data-stu-id="c4fe3-132">-Name</span></span>
<span data-ttu-id="c4fe3-133">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c4fe3-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fe3-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4fe3-134">-PassThru</span></span>
<span data-ttu-id="c4fe3-135">retorna true se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="c4fe3-135">returns true if successful</span></span>

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

### <span data-ttu-id="c4fe3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4fe3-136">-ResourceGroupName</span></span>
<span data-ttu-id="c4fe3-137">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c4fe3-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fe3-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4fe3-138">-ResourceId</span></span>
<span data-ttu-id="c4fe3-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4fe3-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fe3-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="c4fe3-140">-ScanForUpdate</span></span>
<span data-ttu-id="c4fe3-141">Verifica se há atualizações em um dispositivo de borda/gateway stack.</span><span class="sxs-lookup"><span data-stu-id="c4fe3-141">Scans for updates on a Stack edge/gateway device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeScanForUpdateByResourceIdParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fe3-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4fe3-142">-Confirm</span></span>
<span data-ttu-id="c4fe3-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4fe3-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4fe3-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4fe3-144">-WhatIf</span></span>
<span data-ttu-id="c4fe3-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c4fe3-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4fe3-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4fe3-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4fe3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4fe3-147">CommonParameters</span></span>
<span data-ttu-id="c4fe3-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4fe3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4fe3-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4fe3-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4fe3-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4fe3-150">INPUTS</span></span>

### <span data-ttu-id="c4fe3-151">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c4fe3-151">None</span></span>

## <span data-ttu-id="c4fe3-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c4fe3-152">OUTPUTS</span></span>

### <span data-ttu-id="c4fe3-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c4fe3-153">System.Boolean</span></span>

## <span data-ttu-id="c4fe3-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="c4fe3-154">NOTES</span></span>

## <span data-ttu-id="c4fe3-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4fe3-155">RELATED LINKS</span></span>
