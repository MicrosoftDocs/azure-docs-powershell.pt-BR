---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolgeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
ms.openlocfilehash: d1c0b6439b148d51506861a6bfffc6a6681343ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886119"
---
# <span data-ttu-id="d20c9-101">Get-AzSynapseSqlPoolGeoBackup</span><span class="sxs-lookup"><span data-stu-id="d20c9-101">Get-AzSynapseSqlPoolGeoBackup</span></span>

## <span data-ttu-id="d20c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d20c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d20c9-103">Obtém um backup geo-redundante de um Sql Pool.</span><span class="sxs-lookup"><span data-stu-id="d20c9-103">Gets a geo-redundant backup of a Sql Pool.</span></span>

## <span data-ttu-id="d20c9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d20c9-104">SYNTAX</span></span>

### <span data-ttu-id="d20c9-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d20c9-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d20c9-106">SqlPoolGeoBackupResourceId</span><span class="sxs-lookup"><span data-stu-id="d20c9-106">SqlPoolGeoBackupResourceId</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d20c9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d20c9-107">DESCRIPTION</span></span>
<span data-ttu-id="d20c9-108">O cmdlet **Get-AzSynapseSqlPoolGeoBackup** obtém um backup geo-redundante especificado de um Pool SQL ou todos os backups geo-redundantes disponíveis em um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="d20c9-108">The **Get-AzSynapseSqlPoolGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL Pool or all available geo-redundant backups on a specified workspace.</span></span>
<span data-ttu-id="d20c9-109">Um backup geo-redundante é um recurso restaurador usando arquivos de dados de uma localização geográfica separada.</span><span class="sxs-lookup"><span data-stu-id="d20c9-109">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="d20c9-110">Você pode usar Geo-Restore para restaurar um backup geo-redundante no caso de uma paralisação regional para recuperar seu Sql Pool para uma nova região.</span><span class="sxs-lookup"><span data-stu-id="d20c9-110">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your Sql Pool to a new region.</span></span>

## <span data-ttu-id="d20c9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d20c9-111">EXAMPLES</span></span>

### <span data-ttu-id="d20c9-112">Exemplo 1: Obter um backup geo-redundante especificado</span><span class="sxs-lookup"><span data-stu-id="d20c9-112">Example 1: Get a specified geo-redundant backup</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName ContosoResourceGroup -WorkspaceName "ContosoWorkspace" -Name "ContosoSqlPool"
```
<span data-ttu-id="d20c9-113">O cmdlet recupera o Backup Geo para um pool sql.</span><span class="sxs-lookup"><span data-stu-id="d20c9-113">The cmdlet retrieves Geo Backup for a sql pool.</span></span>

### <span data-ttu-id="d20c9-114">Exemplo 2: Obter todos os backups geo-redundantes em um espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d20c9-114">Example 2: Get all geo-redundant backups on a workspace</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="d20c9-115">Esse comando obtém todos os backups geo-redundantes disponíveis em um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="d20c9-115">This command gets all available geo-redundant backups on a specified workspace.</span></span>

### <span data-ttu-id="d20c9-116">Exemplo 3: Obter todos os backups geo-redundantes em um espaço de trabalho usando filtragem</span><span class="sxs-lookup"><span data-stu-id="d20c9-116">Example 3: Get all geo-redundant backups on a workspace using filtering</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Name "Contoso*"
```
<span data-ttu-id="d20c9-117">Este comando obtém todos os backups geo-redundantes disponíveis em um espaço de trabalho especificado que começa com "Contoso".</span><span class="sxs-lookup"><span data-stu-id="d20c9-117">This command gets all available geo-redundant backups on a specified workspace that start with "Contoso".</span></span>

## <span data-ttu-id="d20c9-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d20c9-118">PARAMETERS</span></span>

### <span data-ttu-id="d20c9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d20c9-119">-DefaultProfile</span></span>
<span data-ttu-id="d20c9-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d20c9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d20c9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d20c9-121">-Name</span></span>
<span data-ttu-id="d20c9-122">O pool Sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="d20c9-122">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: The Synapse Sql pool.

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d20c9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d20c9-123">-ResourceId</span></span>
<span data-ttu-id="d20c9-124">Entrada de uma ID de Recurso de Backup Geo do Sql Pool.</span><span class="sxs-lookup"><span data-stu-id="d20c9-124">Input a Sql Pool Geo Backup Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolGeoBackupResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d20c9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d20c9-125">-ResourceGroupName</span></span>
<span data-ttu-id="d20c9-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d20c9-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d20c9-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d20c9-127">-WorkspaceName</span></span>
<span data-ttu-id="d20c9-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="d20c9-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d20c9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d20c9-129">CommonParameters</span></span>
<span data-ttu-id="d20c9-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d20c9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d20c9-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d20c9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d20c9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d20c9-132">INPUTS</span></span>

### <span data-ttu-id="d20c9-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d20c9-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d20c9-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d20c9-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="d20c9-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d20c9-135">OUTPUTS</span></span>

### <span data-ttu-id="d20c9-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span><span class="sxs-lookup"><span data-stu-id="d20c9-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span></span>

## <span data-ttu-id="d20c9-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="d20c9-137">NOTES</span></span>

## <span data-ttu-id="d20c9-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d20c9-138">RELATED LINKS</span></span>
