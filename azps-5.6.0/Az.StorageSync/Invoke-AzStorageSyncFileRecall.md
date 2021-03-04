---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 4da44d6ecff7dbf6de9c0fb20f74988688e9826d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891926"
---
# <span data-ttu-id="0f024-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="0f024-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="0f024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f024-102">SYNOPSIS</span></span>
<span data-ttu-id="0f024-103">Este comando relembra todos os arquivos hierárquiquios de volta para o disco local.</span><span class="sxs-lookup"><span data-stu-id="0f024-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="0f024-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0f024-104">SYNTAX</span></span>

### <span data-ttu-id="0f024-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0f024-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f024-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f024-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f024-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f024-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f024-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0f024-108">DESCRIPTION</span></span>
<span data-ttu-id="0f024-109">Quando a camada de nuvem está habilitada em um ponto de extremidade do servidor (um local específico em um servidor registrado), esse comando pode ser usado para chamar todos os arquivos hierárquiquios para o disco local.</span><span class="sxs-lookup"><span data-stu-id="0f024-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="0f024-110">É altamente recomendável desabilitar a camada de nuvem neste ponto de extremidade do servidor antes de iniciar o recall.</span><span class="sxs-lookup"><span data-stu-id="0f024-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="0f024-111">Se a camada ainda estiver em, o recall pode levar a outros arquivos que estão sendo hierárquidos, o que erra para atingir o objetivo desejado de todo o conteúdo que reside no disco local.</span><span class="sxs-lookup"><span data-stu-id="0f024-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="0f024-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f024-112">EXAMPLES</span></span>

### <span data-ttu-id="0f024-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f024-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="0f024-114">Esse comando recursivamente recorda todos os arquivos hierárcarados localizados no caminho raiz do ponto de extremidade do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="0f024-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="0f024-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0f024-115">PARAMETERS</span></span>

### <span data-ttu-id="0f024-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f024-116">-AsJob</span></span>
<span data-ttu-id="0f024-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0f024-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f024-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f024-118">-DefaultProfile</span></span>
<span data-ttu-id="0f024-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f024-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f024-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f024-120">-InputObject</span></span>
<span data-ttu-id="0f024-121">Objeto SyncGroup, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0f024-121">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="0f024-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0f024-122">-Name</span></span>
<span data-ttu-id="0f024-123">Nome do ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0f024-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="0f024-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f024-124">-PassThru</span></span>
<span data-ttu-id="0f024-125">Em execução normal, esse cmdlet não retorna nenhum valor sobre o sucesso.</span><span class="sxs-lookup"><span data-stu-id="0f024-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="0f024-126">Se você fornecer o parâmetro PassThru, o cmdlet gravará um valor no pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0f024-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="0f024-127">-Pattern</span><span class="sxs-lookup"><span data-stu-id="0f024-127">-Pattern</span></span>
<span data-ttu-id="0f024-128">Padrão do nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="0f024-128">Pattern of the file name</span></span>

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

### <span data-ttu-id="0f024-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="0f024-129">-RecallPath</span></span>
<span data-ttu-id="0f024-130">Caminho de recall que precisa ser chamado.</span><span class="sxs-lookup"><span data-stu-id="0f024-130">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="0f024-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f024-131">-ResourceGroupName</span></span>
<span data-ttu-id="0f024-132">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="0f024-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="0f024-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f024-133">-ResourceId</span></span>
<span data-ttu-id="0f024-134">ID do Recurso ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f024-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="0f024-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="0f024-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="0f024-136">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="0f024-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="0f024-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="0f024-137">-SyncGroupName</span></span>
<span data-ttu-id="0f024-138">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="0f024-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="0f024-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f024-139">-Confirm</span></span>
<span data-ttu-id="0f024-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f024-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f024-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f024-141">-WhatIf</span></span>
<span data-ttu-id="0f024-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0f024-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f024-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f024-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f024-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f024-144">CommonParameters</span></span>
<span data-ttu-id="0f024-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f024-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f024-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f024-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f024-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f024-147">INPUTS</span></span>

### <span data-ttu-id="0f024-148">System.String</span><span class="sxs-lookup"><span data-stu-id="0f024-148">System.String</span></span>

### <span data-ttu-id="0f024-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f024-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="0f024-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0f024-150">OUTPUTS</span></span>

### <span data-ttu-id="0f024-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f024-151">System.Boolean</span></span>

## <span data-ttu-id="0f024-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="0f024-152">NOTES</span></span>

## <span data-ttu-id="0f024-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f024-153">RELATED LINKS</span></span>
