---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: c266b6623463165f14e01e55f0fec4d2d59a581f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774299"
---
# <span data-ttu-id="27ea1-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="27ea1-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="27ea1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="27ea1-103">Esse comando pode ser usado para iniciar manualmente a detecção de alterações de namespaces.</span><span class="sxs-lookup"><span data-stu-id="27ea1-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="27ea1-104">Ele pode ser direcionado para todo o compartilhamento, subpasta ou conjunto de arquivos.</span><span class="sxs-lookup"><span data-stu-id="27ea1-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="27ea1-105">No máximo 10.000 alterações podem ser detectadas.</span><span class="sxs-lookup"><span data-stu-id="27ea1-105">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="27ea1-106">Se o escopo das alterações for conhecido, limite a execução desse comando para partes do namespace, para que a detecção de alteração possa terminar rapidamente e dentro de um limite de alterações do 10.000.</span><span class="sxs-lookup"><span data-stu-id="27ea1-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="27ea1-107">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27ea1-107">SYNTAX</span></span>

### <span data-ttu-id="27ea1-108">StringAndDirectoryParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="27ea1-108">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27ea1-109">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="27ea1-109">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27ea1-110">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="27ea1-110">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27ea1-111">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="27ea1-111">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27ea1-112">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="27ea1-112">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27ea1-113">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="27ea1-113">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27ea1-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27ea1-114">DESCRIPTION</span></span>
<span data-ttu-id="27ea1-115">Periodicamente, a sincronização de arquivos do Azure verifica o namespace dentro de um compartilhamento de arquivos do Azure de sincronização para as alterações que chegavam ao compartilhamento de arquivos por outros meios do que a sincronização. O objetivo é identificar essas alterações e, em última análise, sincronizá-las com os servidores conectados.</span><span class="sxs-lookup"><span data-stu-id="27ea1-115">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="27ea1-116">Esse comando pode ser usado para iniciar manualmente a detecção de alterações de namespaces.</span><span class="sxs-lookup"><span data-stu-id="27ea1-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="27ea1-117">Ele pode ser direcionado para todo o compartilhamento, subpasta ou conjunto de arquivos.</span><span class="sxs-lookup"><span data-stu-id="27ea1-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="27ea1-118">Se o escopo das alterações for conhecido, limite a execução desse comando para partes do namespace, para que a detecção de alteração possa terminar rapidamente e dentro de um limite de alterações do 10.000.</span><span class="sxs-lookup"><span data-stu-id="27ea1-118">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="27ea1-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27ea1-119">EXAMPLES</span></span>

### <span data-ttu-id="27ea1-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="27ea1-120">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="27ea1-121">Neste exemplo, a detecção de alterações é executada nos diretórios "dados" e "Reporting\Templates" de um compartilhamento de arquivos do Azure em sincronização.</span><span class="sxs-lookup"><span data-stu-id="27ea1-121">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="27ea1-122">Todos os caminhos são relativos à raiz do namespace do compartilhamento de arquivos do Azure.</span><span class="sxs-lookup"><span data-stu-id="27ea1-122">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="27ea1-123">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="27ea1-123">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="27ea1-124">Neste exemplo, a detecção de alterações é executada para um conjunto de arquivos conhecidos pelo chamador de comando que foram alterados.</span><span class="sxs-lookup"><span data-stu-id="27ea1-124">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="27ea1-125">O objetivo é fazer com que o Azure File Sync detecte e sincronize essas alterações também.</span><span class="sxs-lookup"><span data-stu-id="27ea1-125">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="27ea1-126">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="27ea1-126">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="27ea1-127">Neste exemplo, a detecção de alterações é executada para o diretório "exemplos" e detecta recursivamente as alterações em subpastas.</span><span class="sxs-lookup"><span data-stu-id="27ea1-127">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="27ea1-128">Lembre-se de que esse comando pode detectar até 10.000 alterações antes de ser anulada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="27ea1-128">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="27ea1-129">Se você suspeitar que há mais de 10.000 alterações, execute o comando em subpartes do namespace.</span><span class="sxs-lookup"><span data-stu-id="27ea1-129">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="27ea1-130">OS</span><span class="sxs-lookup"><span data-stu-id="27ea1-130">PARAMETERS</span></span>

### <span data-ttu-id="27ea1-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27ea1-131">-AsJob</span></span>
<span data-ttu-id="27ea1-132">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="27ea1-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27ea1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ea1-133">-DefaultProfile</span></span>
<span data-ttu-id="27ea1-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27ea1-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27ea1-135">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="27ea1-135">-DirectoryPath</span></span>
<span data-ttu-id="27ea1-136">Diretório em que a detecção de alterações será realizada.</span><span class="sxs-lookup"><span data-stu-id="27ea1-136">Directory where change detection will be performed.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea1-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27ea1-137">-InputObject</span></span>
<span data-ttu-id="27ea1-138">Objeto CloudEndpoint, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="27ea1-138">CloudEndpoint Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: ObjectAndDirectoryParameterSet, ObjectAndPathParameterSet
Aliases: CloudEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27ea1-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="27ea1-139">-Name</span></span>
<span data-ttu-id="27ea1-140">Nome do CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="27ea1-140">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea1-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27ea1-141">-PassThru</span></span>
<span data-ttu-id="27ea1-142">Na execução normal, esse cmdlet retorna nenhum valor de sucesso.</span><span class="sxs-lookup"><span data-stu-id="27ea1-142">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="27ea1-143">Se você fornecer o parâmetro PassThru, o cmdlet irá escrever um valor para o pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="27ea1-143">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="27ea1-144">-Caminho</span><span class="sxs-lookup"><span data-stu-id="27ea1-144">-Path</span></span>
<span data-ttu-id="27ea1-145">Caminho onde a detecção de alterações será realizada.</span><span class="sxs-lookup"><span data-stu-id="27ea1-145">Path where change detection will be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: StringAndPathParameterSet, ResourceIdAndPathParameterSet, ObjectAndPathParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea1-146">-Recursiva</span><span class="sxs-lookup"><span data-stu-id="27ea1-146">-Recursive</span></span>
<span data-ttu-id="27ea1-147">Indicação se a detecção de alterações de diretório é recursiva.</span><span class="sxs-lookup"><span data-stu-id="27ea1-147">Indication whether directory change detection is recursive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea1-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27ea1-148">-ResourceGroupName</span></span>
<span data-ttu-id="27ea1-149">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="27ea1-149">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea1-150">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27ea1-150">-ResourceId</span></span>
<span data-ttu-id="27ea1-151">ID do recurso CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="27ea1-151">CloudEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdAndDirectoryParameterSet, ResourceIdAndPathParameterSet
Aliases: CloudEndpointId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ea1-152">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="27ea1-152">-StorageSyncServiceName</span></span>
<span data-ttu-id="27ea1-153">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="27ea1-153">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea1-154">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="27ea1-154">-SyncGroupName</span></span>
<span data-ttu-id="27ea1-155">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="27ea1-155">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea1-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="27ea1-156">-Confirm</span></span>
<span data-ttu-id="27ea1-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27ea1-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27ea1-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27ea1-158">-WhatIf</span></span>
<span data-ttu-id="27ea1-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="27ea1-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27ea1-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27ea1-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27ea1-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ea1-161">CommonParameters</span></span>
<span data-ttu-id="27ea1-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27ea1-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ea1-163">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27ea1-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ea1-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27ea1-164">INPUTS</span></span>

### <span data-ttu-id="27ea1-165">System. String</span><span class="sxs-lookup"><span data-stu-id="27ea1-165">System.String</span></span>

### <span data-ttu-id="27ea1-166">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="27ea1-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="27ea1-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27ea1-167">OUTPUTS</span></span>

### <span data-ttu-id="27ea1-168">System. void</span><span class="sxs-lookup"><span data-stu-id="27ea1-168">System.Void</span></span>

## <span data-ttu-id="27ea1-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27ea1-169">NOTES</span></span>

## <span data-ttu-id="27ea1-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27ea1-170">RELATED LINKS</span></span>
