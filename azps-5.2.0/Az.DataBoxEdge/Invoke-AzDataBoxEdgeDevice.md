---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 29bf8cf612d3569480c62784466879095ebcdb6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262039"
---
# <span data-ttu-id="61aac-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="61aac-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="61aac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61aac-102">SYNOPSIS</span></span>
<span data-ttu-id="61aac-103">Invoca ações específicas no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61aac-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="61aac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61aac-104">SYNTAX</span></span>

### <span data-ttu-id="61aac-105">InvokeScanForUpdateParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="61aac-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61aac-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61aac-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61aac-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61aac-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61aac-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61aac-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61aac-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="61aac-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61aac-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="61aac-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61aac-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61aac-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61aac-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61aac-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61aac-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61aac-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61aac-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61aac-114">DESCRIPTION</span></span>
<span data-ttu-id="61aac-115">O cmdlet **Invoke-AzDataBoxEdgeDevice** invoca ações para examinar, baixar e instalar as atualizações no dispositivo de borda da caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="61aac-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="61aac-116">Uma verificação automática é executada no dispositivo diariamente, você pode disparar a digitalização explicitamente executando esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61aac-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="61aac-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61aac-117">EXAMPLES</span></span>

### <span data-ttu-id="61aac-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61aac-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="61aac-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="61aac-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="61aac-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="61aac-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="61aac-121">OS</span><span class="sxs-lookup"><span data-stu-id="61aac-121">PARAMETERS</span></span>

### <span data-ttu-id="61aac-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61aac-122">-AsJob</span></span>
<span data-ttu-id="61aac-123">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="61aac-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61aac-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61aac-124">-DefaultProfile</span></span>
<span data-ttu-id="61aac-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61aac-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61aac-126">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="61aac-126">-DeviceObject</span></span>
<span data-ttu-id="61aac-127">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="61aac-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="61aac-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="61aac-128">-FetchUpdate</span></span>
<span data-ttu-id="61aac-129">Baixa as atualizações em um dispositivo de borda/gateway de caixa de dados</span><span class="sxs-lookup"><span data-stu-id="61aac-129">Downloads the updates on a data box edge/gateway device</span></span>

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

### <span data-ttu-id="61aac-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="61aac-130">-InstallUpdate</span></span>
<span data-ttu-id="61aac-131">Instala as atualizações na caixa de dados dispositivo de borda/gateway</span><span class="sxs-lookup"><span data-stu-id="61aac-131">Installs the updates on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="61aac-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="61aac-132">-Name</span></span>
<span data-ttu-id="61aac-133">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="61aac-133">Device Name</span></span>

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

### <span data-ttu-id="61aac-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61aac-134">-PassThru</span></span>
<span data-ttu-id="61aac-135">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="61aac-135">returns true if successful</span></span>

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

### <span data-ttu-id="61aac-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61aac-136">-ResourceGroupName</span></span>
<span data-ttu-id="61aac-137">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="61aac-137">Resource Group Name</span></span>

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

### <span data-ttu-id="61aac-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61aac-138">-ResourceId</span></span>
<span data-ttu-id="61aac-139">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="61aac-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="61aac-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="61aac-140">-ScanForUpdate</span></span>
<span data-ttu-id="61aac-141">Verifica se há atualizações em um dispositivo de borda/gateway de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="61aac-141">Scans for updates on a data box edge/gateway device.</span></span>

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

### <span data-ttu-id="61aac-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="61aac-142">-Confirm</span></span>
<span data-ttu-id="61aac-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61aac-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61aac-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61aac-144">-WhatIf</span></span>
<span data-ttu-id="61aac-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="61aac-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61aac-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="61aac-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61aac-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61aac-147">CommonParameters</span></span>
<span data-ttu-id="61aac-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61aac-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61aac-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61aac-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61aac-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61aac-150">INPUTS</span></span>

### <span data-ttu-id="61aac-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="61aac-151">None</span></span>

## <span data-ttu-id="61aac-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61aac-152">OUTPUTS</span></span>

### <span data-ttu-id="61aac-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="61aac-153">System.Boolean</span></span>

## <span data-ttu-id="61aac-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61aac-154">NOTES</span></span>

## <span data-ttu-id="61aac-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61aac-155">RELATED LINKS</span></span>
