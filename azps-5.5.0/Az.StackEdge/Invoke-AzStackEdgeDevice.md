---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: f25aeb501ff046a25330ad5db47bbdb06fbe7b35
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118916"
---
# <span data-ttu-id="3e00d-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3e00d-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="3e00d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e00d-102">SYNOPSIS</span></span>
<span data-ttu-id="3e00d-103">Invoca ações específicas no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e00d-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="3e00d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e00d-104">SYNTAX</span></span>

### <span data-ttu-id="3e00d-105">InvokeScanForUpdateParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3e00d-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e00d-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e00d-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e00d-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e00d-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e00d-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e00d-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e00d-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e00d-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e00d-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e00d-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e00d-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e00d-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e00d-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e00d-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e00d-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e00d-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e00d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e00d-114">DESCRIPTION</span></span>
<span data-ttu-id="3e00d-115">O cmdlet **Invoke-AzSt stackEdgeDevice** invoca ações para verificar, baixar e instalar as atualizações no dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="3e00d-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="3e00d-116">Uma verificação automática é feita diariamente no dispositivo, você pode acionar a verificação explicitamente executando este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e00d-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="3e00d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3e00d-117">EXAMPLES</span></span>

### <span data-ttu-id="3e00d-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3e00d-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="3e00d-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3e00d-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="3e00d-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3e00d-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="3e00d-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e00d-121">PARAMETERS</span></span>

### <span data-ttu-id="3e00d-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e00d-122">-AsJob</span></span>
<span data-ttu-id="3e00d-123">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3e00d-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e00d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e00d-124">-DefaultProfile</span></span>
<span data-ttu-id="3e00d-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e00d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e00d-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="3e00d-126">-DeviceObject</span></span>
<span data-ttu-id="3e00d-127">Forneça o objeto do dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="3e00d-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="3e00d-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="3e00d-128">-FetchUpdate</span></span>
<span data-ttu-id="3e00d-129">Baixa as atualizações em um dispositivo stack edge/gateway</span><span class="sxs-lookup"><span data-stu-id="3e00d-129">Downloads the updates on a Stack edge/gateway device</span></span>

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

### <span data-ttu-id="3e00d-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="3e00d-130">-InstallUpdate</span></span>
<span data-ttu-id="3e00d-131">Instala as atualizações no dispositivo stack edge/gateway</span><span class="sxs-lookup"><span data-stu-id="3e00d-131">Installs the updates on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="3e00d-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e00d-132">-Name</span></span>
<span data-ttu-id="3e00d-133">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="3e00d-133">Device Name</span></span>

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

### <span data-ttu-id="3e00d-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e00d-134">-PassThru</span></span>
<span data-ttu-id="3e00d-135">retorna verdadeiro se for bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="3e00d-135">returns true if successful</span></span>

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

### <span data-ttu-id="3e00d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e00d-136">-ResourceGroupName</span></span>
<span data-ttu-id="3e00d-137">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="3e00d-137">Resource Group Name</span></span>

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

### <span data-ttu-id="3e00d-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e00d-138">-ResourceId</span></span>
<span data-ttu-id="3e00d-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e00d-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="3e00d-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="3e00d-140">-ScanForUpdate</span></span>
<span data-ttu-id="3e00d-141">Verifica se há atualizações em um dispositivo stack edge/gateway.</span><span class="sxs-lookup"><span data-stu-id="3e00d-141">Scans for updates on a Stack edge/gateway device.</span></span>

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

### <span data-ttu-id="3e00d-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3e00d-142">-Confirm</span></span>
<span data-ttu-id="3e00d-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e00d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e00d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e00d-144">-WhatIf</span></span>
<span data-ttu-id="3e00d-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3e00d-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e00d-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e00d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e00d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e00d-147">CommonParameters</span></span>
<span data-ttu-id="3e00d-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e00d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e00d-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e00d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e00d-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="3e00d-150">INPUTS</span></span>

### <span data-ttu-id="3e00d-151">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3e00d-151">None</span></span>

## <span data-ttu-id="3e00d-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="3e00d-152">OUTPUTS</span></span>

### <span data-ttu-id="3e00d-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3e00d-153">System.Boolean</span></span>

## <span data-ttu-id="3e00d-154">Notas</span><span class="sxs-lookup"><span data-stu-id="3e00d-154">NOTES</span></span>

## <span data-ttu-id="3e00d-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e00d-155">RELATED LINKS</span></span>
