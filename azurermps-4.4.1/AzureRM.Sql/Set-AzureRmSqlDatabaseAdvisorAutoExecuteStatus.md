---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 149579bb6bbcd4ee5fe5fa192ad040e6e4c68b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441369"
---
# <span data-ttu-id="f9a61-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f9a61-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="f9a61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9a61-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a61-103">Modifica o status de execução automática de um supervisor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9a61-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9a61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9a61-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9a61-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9a61-105">DESCRIPTION</span></span>
<span data-ttu-id="f9a61-106">O cmdlet **set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** modifica a propriedade de execução automática para um supervisor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9a61-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="f9a61-107">Atualmente, esse cmdlet dá suporte a valores habilitados, desabilitados e padrão.</span><span class="sxs-lookup"><span data-stu-id="f9a61-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="f9a61-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9a61-108">EXAMPLES</span></span>

### <span data-ttu-id="f9a61-109">Exemplo 1: habilitar a execução automática para um conselheiro</span><span class="sxs-lookup"><span data-stu-id="f9a61-109">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="f9a61-110">Esse comando altera o status de execução automática de um supervisor chamado CreateIndex para Enabled.</span><span class="sxs-lookup"><span data-stu-id="f9a61-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="f9a61-111">OS</span><span class="sxs-lookup"><span data-stu-id="f9a61-111">PARAMETERS</span></span>

### <span data-ttu-id="f9a61-112">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="f9a61-112">-AdvisorName</span></span>
<span data-ttu-id="f9a61-113">Especifica o nome do supervisor para o qual esse cmdlet modifica o status.</span><span class="sxs-lookup"><span data-stu-id="f9a61-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a61-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f9a61-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="f9a61-115">Especifica o valor do status.</span><span class="sxs-lookup"><span data-stu-id="f9a61-115">Specifies the value for the status.</span></span>
<span data-ttu-id="f9a61-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f9a61-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f9a61-117">Possibilita</span><span class="sxs-lookup"><span data-stu-id="f9a61-117">Enabled</span></span> 
- <span data-ttu-id="f9a61-118">Ativo</span><span class="sxs-lookup"><span data-stu-id="f9a61-118">Disabled</span></span> 
- <span data-ttu-id="f9a61-119">Assume</span><span class="sxs-lookup"><span data-stu-id="f9a61-119">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a61-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f9a61-120">-DatabaseName</span></span>
<span data-ttu-id="f9a61-121">Especifica o nome do banco de dados para o qual esse cmdlet modifica o status.</span><span class="sxs-lookup"><span data-stu-id="f9a61-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a61-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9a61-122">-ResourceGroupName</span></span>
<span data-ttu-id="f9a61-123">Especifica o nome do grupo de recursos do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9a61-123">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a61-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f9a61-124">-ServerName</span></span>
<span data-ttu-id="f9a61-125">Especifica o nome do servidor do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9a61-125">Specifies the name of the server for the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a61-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f9a61-126">-Confirm</span></span>
<span data-ttu-id="f9a61-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9a61-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9a61-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9a61-128">-WhatIf</span></span>
<span data-ttu-id="f9a61-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f9a61-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9a61-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9a61-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9a61-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a61-131">-DefaultProfile</span></span>
<span data-ttu-id="f9a61-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9a61-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a61-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a61-133">CommonParameters</span></span>
<span data-ttu-id="f9a61-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a61-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a61-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9a61-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a61-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9a61-136">INPUTS</span></span>

## <span data-ttu-id="f9a61-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9a61-137">OUTPUTS</span></span>

### <span data-ttu-id="f9a61-138">Microsoft. Azure. Commands. Sql. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="f9a61-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>
<span data-ttu-id="f9a61-139">Esse cmdlet retorna um objeto **AzureSqlDatabaseAdvisorModel** .</span><span class="sxs-lookup"><span data-stu-id="f9a61-139">This cmdlet returns an **AzureSqlDatabaseAdvisorModel** object.</span></span>

## <span data-ttu-id="f9a61-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9a61-140">NOTES</span></span>

## <span data-ttu-id="f9a61-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9a61-141">RELATED LINKS</span></span>

[<span data-ttu-id="f9a61-142">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="f9a61-142">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="f9a61-143">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f9a61-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
