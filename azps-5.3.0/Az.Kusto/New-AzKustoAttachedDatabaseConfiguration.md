---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 09284a91c5ea2f7561a867250a92c4cd0d96e8e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433582"
---
# <span data-ttu-id="157b6-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="157b6-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="157b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="157b6-102">SYNOPSIS</span></span>
<span data-ttu-id="157b6-103">Cria ou atualiza uma configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="157b6-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="157b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="157b6-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="157b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="157b6-105">DESCRIPTION</span></span>
<span data-ttu-id="157b6-106">Cria ou atualiza uma configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="157b6-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="157b6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="157b6-107">EXAMPLES</span></span>

### <span data-ttu-id="157b6-108">Exemplo 1: criar um novo AttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="157b6-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="157b6-109">O comando acima cria um banco de dados ReadOnly "mykustodatabase" no cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="157b6-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="157b6-110">Ele segue o banco de dados "mykustodatabase" do cluster "testnewkustocluster"</span><span class="sxs-lookup"><span data-stu-id="157b6-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="157b6-111">OS</span><span class="sxs-lookup"><span data-stu-id="157b6-111">PARAMETERS</span></span>

### <span data-ttu-id="157b6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="157b6-112">-AsJob</span></span>
<span data-ttu-id="157b6-113">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="157b6-113">Run the command as a job</span></span>

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

### <span data-ttu-id="157b6-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="157b6-114">-ClusterName</span></span>
<span data-ttu-id="157b6-115">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="157b6-115">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157b6-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="157b6-116">-ClusterResourceId</span></span>
<span data-ttu-id="157b6-117">A ID do recurso do cluster em que os bancos de dados que você deseja anexar residem.</span><span class="sxs-lookup"><span data-stu-id="157b6-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="157b6-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="157b6-118">-DatabaseName</span></span>
<span data-ttu-id="157b6-119">O nome do banco de dados que você deseja anexar, use \* se quiser acompanhar todos os bancos de dados atuais e futuros.</span><span class="sxs-lookup"><span data-stu-id="157b6-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="157b6-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="157b6-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="157b6-121">O tipo de modificação de entidades de segurança padrão</span><span class="sxs-lookup"><span data-stu-id="157b6-121">The default principals modification kind</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DefaultPrincipalsModificationKind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157b6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="157b6-122">-DefaultProfile</span></span>
<span data-ttu-id="157b6-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="157b6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157b6-124">-Local</span><span class="sxs-lookup"><span data-stu-id="157b6-124">-Location</span></span>
<span data-ttu-id="157b6-125">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="157b6-125">Resource location.</span></span>

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

### <span data-ttu-id="157b6-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="157b6-126">-Name</span></span>
<span data-ttu-id="157b6-127">O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="157b6-127">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157b6-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="157b6-128">-NoWait</span></span>
<span data-ttu-id="157b6-129">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="157b6-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="157b6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="157b6-130">-ResourceGroupName</span></span>
<span data-ttu-id="157b6-131">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="157b6-131">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157b6-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="157b6-132">-SubscriptionId</span></span>
<span data-ttu-id="157b6-133">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="157b6-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="157b6-134">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="157b6-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157b6-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="157b6-135">-Confirm</span></span>
<span data-ttu-id="157b6-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="157b6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="157b6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="157b6-137">-WhatIf</span></span>
<span data-ttu-id="157b6-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="157b6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="157b6-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="157b6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="157b6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="157b6-140">CommonParameters</span></span>
<span data-ttu-id="157b6-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="157b6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="157b6-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="157b6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="157b6-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="157b6-143">INPUTS</span></span>

## <span data-ttu-id="157b6-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="157b6-144">OUTPUTS</span></span>

### <span data-ttu-id="157b6-145">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200918. IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="157b6-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="157b6-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="157b6-146">NOTES</span></span>

<span data-ttu-id="157b6-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="157b6-147">ALIASES</span></span>

## <span data-ttu-id="157b6-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="157b6-148">RELATED LINKS</span></span>

