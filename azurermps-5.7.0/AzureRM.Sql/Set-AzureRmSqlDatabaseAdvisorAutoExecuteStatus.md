---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 7af5736e2f66b8bf428815456ba95b3c5b4b6182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602342"
---
# <span data-ttu-id="f187e-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f187e-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="f187e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f187e-102">SYNOPSIS</span></span>
<span data-ttu-id="f187e-103">Modifica o status de execução automática de um supervisor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f187e-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f187e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f187e-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f187e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f187e-105">DESCRIPTION</span></span>
<span data-ttu-id="f187e-106">O cmdlet **set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** modifica a propriedade de execução automática para um supervisor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f187e-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="f187e-107">Atualmente, esse cmdlet dá suporte a valores habilitados, desabilitados e padrão.</span><span class="sxs-lookup"><span data-stu-id="f187e-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="f187e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f187e-108">EXAMPLES</span></span>

### <span data-ttu-id="f187e-109">Exemplo 1: habilitar a execução automática para um conselheiro</span><span class="sxs-lookup"><span data-stu-id="f187e-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="f187e-110">Esse comando altera o status de execução automática de um supervisor chamado CreateIndex para Enabled.</span><span class="sxs-lookup"><span data-stu-id="f187e-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="f187e-111">OS</span><span class="sxs-lookup"><span data-stu-id="f187e-111">PARAMETERS</span></span>

### <span data-ttu-id="f187e-112">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="f187e-112">-AdvisorName</span></span>
<span data-ttu-id="f187e-113">Especifica o nome do supervisor para o qual esse cmdlet modifica o status.</span><span class="sxs-lookup"><span data-stu-id="f187e-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="f187e-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f187e-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="f187e-115">Especifica o valor do status.</span><span class="sxs-lookup"><span data-stu-id="f187e-115">Specifies the value for the status.</span></span>
<span data-ttu-id="f187e-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f187e-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f187e-117">Possibilita</span><span class="sxs-lookup"><span data-stu-id="f187e-117">Enabled</span></span> 
- <span data-ttu-id="f187e-118">Ativo</span><span class="sxs-lookup"><span data-stu-id="f187e-118">Disabled</span></span> 
- <span data-ttu-id="f187e-119">Assume</span><span class="sxs-lookup"><span data-stu-id="f187e-119">Default</span></span>

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

### <span data-ttu-id="f187e-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f187e-120">-DatabaseName</span></span>
<span data-ttu-id="f187e-121">Especifica o nome do banco de dados para o qual esse cmdlet modifica o status.</span><span class="sxs-lookup"><span data-stu-id="f187e-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="f187e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f187e-122">-DefaultProfile</span></span>
<span data-ttu-id="f187e-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f187e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f187e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f187e-124">-ResourceGroupName</span></span>
<span data-ttu-id="f187e-125">Especifica o nome do grupo de recursos do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f187e-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="f187e-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f187e-126">-ServerName</span></span>
<span data-ttu-id="f187e-127">Especifica o nome do servidor do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f187e-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="f187e-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f187e-128">-Confirm</span></span>
<span data-ttu-id="f187e-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f187e-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f187e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f187e-130">-WhatIf</span></span>
<span data-ttu-id="f187e-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f187e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f187e-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f187e-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f187e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f187e-133">CommonParameters</span></span>
<span data-ttu-id="f187e-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f187e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f187e-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f187e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f187e-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f187e-136">INPUTS</span></span>

### <span data-ttu-id="f187e-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f187e-137">None</span></span>
<span data-ttu-id="f187e-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f187e-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f187e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f187e-139">OUTPUTS</span></span>

### <span data-ttu-id="f187e-140">Microsoft. Azure. Commands. Sql. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="f187e-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>
<span data-ttu-id="f187e-141">Esse cmdlet retorna um objeto **AzureSqlDatabaseAdvisorModel** .</span><span class="sxs-lookup"><span data-stu-id="f187e-141">This cmdlet returns an **AzureSqlDatabaseAdvisorModel** object.</span></span>

## <span data-ttu-id="f187e-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f187e-142">NOTES</span></span>

## <span data-ttu-id="f187e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f187e-143">RELATED LINKS</span></span>

[<span data-ttu-id="f187e-144">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="f187e-144">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="f187e-145">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f187e-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

