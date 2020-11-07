---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 06eb3942a5320ff7c5c8bb3d089ecad2da912edb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774297"
---
# <span data-ttu-id="fe406-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="fe406-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="fe406-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe406-102">SYNOPSIS</span></span>
<span data-ttu-id="fe406-103">Esse comando recupera novamente todos os arquivos em camadas para o disco local.</span><span class="sxs-lookup"><span data-stu-id="fe406-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="fe406-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe406-104">SYNTAX</span></span>

### <span data-ttu-id="fe406-105">StringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fe406-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe406-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe406-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe406-107">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="fe406-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe406-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe406-108">DESCRIPTION</span></span>
<span data-ttu-id="fe406-109">Quando a hierarquização na nuvem está habilitada em um ponto de extremidade do servidor (um local específico em um servidor registrado), esse comando pode ser usado para cancelar todos os arquivos em camadas para o disco local.</span><span class="sxs-lookup"><span data-stu-id="fe406-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="fe406-110">É altamente recomendável desabilitar a hierarquização na nuvem neste ponto de extremidade do servidor antes de iniciar a cancelamento.</span><span class="sxs-lookup"><span data-stu-id="fe406-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="fe406-111">Se a hierarquização ainda estiver ativada, a cancelamento pode levar a outros arquivos em camadas que não conseguem alcançar a meta desejada de todo o conteúdo que reside no disco local.</span><span class="sxs-lookup"><span data-stu-id="fe406-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="fe406-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe406-112">EXAMPLES</span></span>

### <span data-ttu-id="fe406-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe406-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="fe406-114">Esse comando recupera recursivamente todos os arquivos em camadas localizados sob o caminho raiz do ponto de extremidade do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="fe406-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="fe406-115">OS</span><span class="sxs-lookup"><span data-stu-id="fe406-115">PARAMETERS</span></span>

### <span data-ttu-id="fe406-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe406-116">-AsJob</span></span>
<span data-ttu-id="fe406-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fe406-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe406-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe406-118">-DefaultProfile</span></span>
<span data-ttu-id="fe406-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe406-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe406-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe406-120">-InputObject</span></span>
<span data-ttu-id="fe406-121">Objeto de objeto de sincronização, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fe406-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer, ServerEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe406-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe406-122">-Name</span></span>
<span data-ttu-id="fe406-123">Nome do ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="fe406-123">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe406-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe406-124">-PassThru</span></span>
<span data-ttu-id="fe406-125">Na execução normal, esse cmdlet retorna nenhum valor de sucesso.</span><span class="sxs-lookup"><span data-stu-id="fe406-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="fe406-126">Se você fornecer o parâmetro PassThru, o cmdlet irá escrever um valor para o pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fe406-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="fe406-127">-Padrão</span><span class="sxs-lookup"><span data-stu-id="fe406-127">-Pattern</span></span>
<span data-ttu-id="fe406-128">Padrão do nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="fe406-128">Pattern of the file name</span></span>

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

### <span data-ttu-id="fe406-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="fe406-129">-RecallPath</span></span>
<span data-ttu-id="fe406-130">Cancelar o caminho que precisa ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="fe406-130">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="fe406-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe406-131">-ResourceGroupName</span></span>
<span data-ttu-id="fe406-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe406-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe406-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe406-133">-ResourceId</span></span>
<span data-ttu-id="fe406-134">ID do recurso ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe406-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe406-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="fe406-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="fe406-136">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="fe406-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe406-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="fe406-137">-SyncGroupName</span></span>
<span data-ttu-id="fe406-138">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="fe406-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe406-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fe406-139">-Confirm</span></span>
<span data-ttu-id="fe406-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe406-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe406-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe406-141">-WhatIf</span></span>
<span data-ttu-id="fe406-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fe406-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe406-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe406-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe406-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe406-144">CommonParameters</span></span>
<span data-ttu-id="fe406-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe406-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe406-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe406-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe406-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe406-147">INPUTS</span></span>

### <span data-ttu-id="fe406-148">System. String</span><span class="sxs-lookup"><span data-stu-id="fe406-148">System.String</span></span>

### <span data-ttu-id="fe406-149">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe406-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="fe406-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe406-150">OUTPUTS</span></span>

### <span data-ttu-id="fe406-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe406-151">System.Boolean</span></span>

## <span data-ttu-id="fe406-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe406-152">NOTES</span></span>

## <span data-ttu-id="fe406-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe406-153">RELATED LINKS</span></span>
