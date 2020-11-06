---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 7b4d445ede7bae59431707f3ff6bc587effde21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431547"
---
# <span data-ttu-id="e36d4-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e36d4-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="e36d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e36d4-102">SYNOPSIS</span></span>
<span data-ttu-id="e36d4-103">Atualiza o status de execução automática de um supervisor de pool elástico do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e36d4-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e36d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e36d4-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e36d4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e36d4-105">DESCRIPTION</span></span>
<span data-ttu-id="e36d4-106">O cmdlet **set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** define a propriedade auto execute para um supervisor de pool elástico do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e36d4-106">The **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="e36d4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e36d4-107">EXAMPLES</span></span>

### <span data-ttu-id="e36d4-108">Exemplo 1: habilitar a execução automática para um conselheiro</span><span class="sxs-lookup"><span data-stu-id="e36d4-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
'Enabled'ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : ElasticPool
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="e36d4-109">Esse comando define o status de execução automática de um supervisor chamado CreateIndex como Enabled.</span><span class="sxs-lookup"><span data-stu-id="e36d4-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="e36d4-110">OS</span><span class="sxs-lookup"><span data-stu-id="e36d4-110">PARAMETERS</span></span>

### <span data-ttu-id="e36d4-111">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="e36d4-111">-AdvisorName</span></span>
<span data-ttu-id="e36d4-112">Especifica o nome do supervisor para o qual esse cmdlet atualiza o status de execução automática.</span><span class="sxs-lookup"><span data-stu-id="e36d4-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e36d4-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e36d4-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="e36d4-114">Especifica um novo valor para o qual esse cmdlet atualiza o status de execução automática.</span><span class="sxs-lookup"><span data-stu-id="e36d4-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="e36d4-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e36d4-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e36d4-116">Possibilita</span><span class="sxs-lookup"><span data-stu-id="e36d4-116">Enabled</span></span>
- <span data-ttu-id="e36d4-117">Ativo</span><span class="sxs-lookup"><span data-stu-id="e36d4-117">Disabled</span></span>
- <span data-ttu-id="e36d4-118">Assume</span><span class="sxs-lookup"><span data-stu-id="e36d4-118">Default</span></span>

```yaml
Type: AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e36d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36d4-119">-DefaultProfile</span></span>
<span data-ttu-id="e36d4-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e36d4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36d4-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e36d4-121">-ElasticPoolName</span></span>
<span data-ttu-id="e36d4-122">Especifica o nome do pool elástico.</span><span class="sxs-lookup"><span data-stu-id="e36d4-122">Specifies the name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e36d4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e36d4-123">-ResourceGroupName</span></span>
<span data-ttu-id="e36d4-124">Especifica o nome do grupo de recursos do servidor que contém esse pool elástico.</span><span class="sxs-lookup"><span data-stu-id="e36d4-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e36d4-125">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e36d4-125">-ServerName</span></span>
<span data-ttu-id="e36d4-126">Especifica o nome do servidor no qual o pool elástico está.</span><span class="sxs-lookup"><span data-stu-id="e36d4-126">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e36d4-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e36d4-127">-Confirm</span></span>
<span data-ttu-id="e36d4-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e36d4-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36d4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e36d4-129">-WhatIf</span></span>
<span data-ttu-id="e36d4-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e36d4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e36d4-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e36d4-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36d4-132">CommonParameters</span></span>
<span data-ttu-id="e36d4-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e36d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36d4-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e36d4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36d4-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e36d4-135">INPUTS</span></span>

### <span data-ttu-id="e36d4-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e36d4-136">None</span></span>
<span data-ttu-id="e36d4-137">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e36d4-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e36d4-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e36d4-138">OUTPUTS</span></span>

### <span data-ttu-id="e36d4-139">Microsoft. Azure. Commands. Sql. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="e36d4-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="e36d4-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e36d4-140">NOTES</span></span>
* <span data-ttu-id="e36d4-141">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, pool elástico, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="e36d4-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="e36d4-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e36d4-142">RELATED LINKS</span></span>

[<span data-ttu-id="e36d4-143">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="e36d4-143">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="e36d4-144">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e36d4-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
