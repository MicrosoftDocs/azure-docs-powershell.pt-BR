---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 29bf8cf612d3569480c62784466879095ebcdb6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115441"
---
# <span data-ttu-id="c1fa7-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c1fa7-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="c1fa7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1fa7-102">SYNOPSIS</span></span>
<span data-ttu-id="c1fa7-103">Invoca ações específicas no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1fa7-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="c1fa7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1fa7-104">SYNTAX</span></span>

### <span data-ttu-id="c1fa7-105">InvokeScanForUpdateParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c1fa7-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1fa7-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1fa7-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1fa7-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1fa7-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1fa7-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1fa7-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1fa7-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1fa7-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1fa7-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1fa7-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1fa7-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1fa7-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1fa7-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1fa7-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1fa7-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1fa7-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1fa7-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1fa7-114">DESCRIPTION</span></span>
<span data-ttu-id="c1fa7-115">O cmdlet **Invoke-AzDataBoxEdgeDevice** invoca ações para verificar, baixar e instalar as atualizações no dispositivo De borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="c1fa7-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="c1fa7-116">Uma verificação automática é feita diariamente no dispositivo, você pode acionar a verificação explicitamente executando este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1fa7-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="c1fa7-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c1fa7-117">EXAMPLES</span></span>

### <span data-ttu-id="c1fa7-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1fa7-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="c1fa7-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c1fa7-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="c1fa7-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c1fa7-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="c1fa7-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1fa7-121">PARAMETERS</span></span>

### <span data-ttu-id="c1fa7-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1fa7-122">-AsJob</span></span>
<span data-ttu-id="c1fa7-123">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c1fa7-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1fa7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1fa7-124">-DefaultProfile</span></span>
<span data-ttu-id="c1fa7-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1fa7-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1fa7-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c1fa7-126">-DeviceObject</span></span>
<span data-ttu-id="c1fa7-127">Forneça o objeto do dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="c1fa7-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1fa7-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="c1fa7-128">-FetchUpdate</span></span>
<span data-ttu-id="c1fa7-129">Baixa as atualizações em um dispositivo de borda/gateway de caixa de dados</span><span class="sxs-lookup"><span data-stu-id="c1fa7-129">Downloads the updates on a data box edge/gateway device</span></span>

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

### <span data-ttu-id="c1fa7-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="c1fa7-130">-InstallUpdate</span></span>
<span data-ttu-id="c1fa7-131">Instala as atualizações na borda da caixa de dados/dispositivo de gateway</span><span class="sxs-lookup"><span data-stu-id="c1fa7-131">Installs the updates on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="c1fa7-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1fa7-132">-Name</span></span>
<span data-ttu-id="c1fa7-133">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c1fa7-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1fa7-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1fa7-134">-PassThru</span></span>
<span data-ttu-id="c1fa7-135">retorna verdadeiro se for bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="c1fa7-135">returns true if successful</span></span>

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

### <span data-ttu-id="c1fa7-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1fa7-136">-ResourceGroupName</span></span>
<span data-ttu-id="c1fa7-137">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c1fa7-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1fa7-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1fa7-138">-ResourceId</span></span>
<span data-ttu-id="c1fa7-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1fa7-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1fa7-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="c1fa7-140">-ScanForUpdate</span></span>
<span data-ttu-id="c1fa7-141">Verifica se há atualizações em um dispositivo de borda/gateway de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="c1fa7-141">Scans for updates on a data box edge/gateway device.</span></span>

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

### <span data-ttu-id="c1fa7-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c1fa7-142">-Confirm</span></span>
<span data-ttu-id="c1fa7-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1fa7-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1fa7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1fa7-144">-WhatIf</span></span>
<span data-ttu-id="c1fa7-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c1fa7-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1fa7-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1fa7-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1fa7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1fa7-147">CommonParameters</span></span>
<span data-ttu-id="c1fa7-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1fa7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1fa7-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1fa7-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1fa7-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="c1fa7-150">INPUTS</span></span>

### <span data-ttu-id="c1fa7-151">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c1fa7-151">None</span></span>

## <span data-ttu-id="c1fa7-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="c1fa7-152">OUTPUTS</span></span>

### <span data-ttu-id="c1fa7-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1fa7-153">System.Boolean</span></span>

## <span data-ttu-id="c1fa7-154">Notas</span><span class="sxs-lookup"><span data-stu-id="c1fa7-154">NOTES</span></span>

## <span data-ttu-id="c1fa7-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1fa7-155">RELATED LINKS</span></span>
