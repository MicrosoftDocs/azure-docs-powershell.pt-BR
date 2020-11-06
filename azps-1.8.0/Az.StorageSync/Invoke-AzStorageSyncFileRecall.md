---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 5463c20274f60c2d6fb6c4807bf2c4d27da76808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598493"
---
# <span data-ttu-id="72266-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="72266-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="72266-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72266-102">SYNOPSIS</span></span>
<span data-ttu-id="72266-103">Esse comando recupera novamente todos os arquivos em camadas para o disco local.</span><span class="sxs-lookup"><span data-stu-id="72266-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="72266-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72266-104">SYNTAX</span></span>

### <span data-ttu-id="72266-105">Objectparameterset (padrão)</span><span class="sxs-lookup"><span data-stu-id="72266-105">ObjectParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72266-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="72266-106">StringParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72266-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72266-107">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72266-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72266-108">DESCRIPTION</span></span>
<span data-ttu-id="72266-109">Quando a hierarquização na nuvem está habilitada em um ponto de extremidade do servidor (um local específico em um servidor registrado), esse comando pode ser usado para cancelar todos os arquivos em camadas para o disco local.</span><span class="sxs-lookup"><span data-stu-id="72266-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="72266-110">É altamente recomendável desabilitar a hierarquização na nuvem neste ponto de extremidade do servidor antes de iniciar a cancelamento.</span><span class="sxs-lookup"><span data-stu-id="72266-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="72266-111">Se a hierarquização ainda estiver ativada, a cancelamento pode levar a outros arquivos em camadas que não conseguem alcançar a meta desejada de todo o conteúdo que reside no disco local.</span><span class="sxs-lookup"><span data-stu-id="72266-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="72266-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72266-112">EXAMPLES</span></span>

### <span data-ttu-id="72266-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="72266-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="72266-114">Esse comando recupera recursivamente todos os arquivos em camadas localizados sob o caminho raiz do ponto de extremidade do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="72266-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="72266-115">OS</span><span class="sxs-lookup"><span data-stu-id="72266-115">PARAMETERS</span></span>

### <span data-ttu-id="72266-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72266-116">-AsJob</span></span>
<span data-ttu-id="72266-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="72266-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72266-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72266-118">-DefaultProfile</span></span>
<span data-ttu-id="72266-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="72266-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72266-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72266-120">-InputObject</span></span>
<span data-ttu-id="72266-121">Objeto de objeto de sincronização, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="72266-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72266-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="72266-122">-Name</span></span>
<span data-ttu-id="72266-123">Nome do ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="72266-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="72266-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72266-124">-PassThru</span></span>
<span data-ttu-id="72266-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="72266-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="72266-126">-Padrão</span><span class="sxs-lookup"><span data-stu-id="72266-126">-Pattern</span></span>
<span data-ttu-id="72266-127">Padrão do nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="72266-127">Pattern of the file name</span></span>

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

### <span data-ttu-id="72266-128">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="72266-128">-RecallPath</span></span>
<span data-ttu-id="72266-129">Cancelar o caminho que precisa ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="72266-129">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="72266-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72266-130">-ResourceGroupName</span></span>
<span data-ttu-id="72266-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="72266-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="72266-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72266-132">-ResourceId</span></span>
<span data-ttu-id="72266-133">ID do recurso ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="72266-133">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="72266-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="72266-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="72266-135">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="72266-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="72266-136">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="72266-136">-SyncGroupName</span></span>
<span data-ttu-id="72266-137">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="72266-137">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="72266-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72266-138">CommonParameters</span></span>
<span data-ttu-id="72266-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72266-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72266-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72266-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72266-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72266-141">INPUTS</span></span>

### <span data-ttu-id="72266-142">System. String</span><span class="sxs-lookup"><span data-stu-id="72266-142">System.String</span></span>

### <span data-ttu-id="72266-143">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="72266-143">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="72266-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72266-144">OUTPUTS</span></span>

### <span data-ttu-id="72266-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72266-145">System.Boolean</span></span>

## <span data-ttu-id="72266-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72266-146">NOTES</span></span>

## <span data-ttu-id="72266-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72266-147">RELATED LINKS</span></span>
