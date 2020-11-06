---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: f483d3deb6c4e4ee6fb5c091dffc9b7969766d6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431762"
---
# <span data-ttu-id="e819e-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e819e-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="e819e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e819e-102">SYNOPSIS</span></span>
<span data-ttu-id="e819e-103">Atualiza o status de execução automática de um supervisor do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="e819e-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e819e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e819e-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e819e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e819e-105">DESCRIPTION</span></span>
<span data-ttu-id="e819e-106">O cmdlet **set-AzureRmSqlServerAdvisorAutoExecuteStatus** define a propriedade auto execute para um SQL Server Advisor do Azure.</span><span class="sxs-lookup"><span data-stu-id="e819e-106">The **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="e819e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e819e-107">EXAMPLES</span></span>

### <span data-ttu-id="e819e-108">Exemplo 1: habilitar a execução automática para um conselheiro</span><span class="sxs-lookup"><span data-stu-id="e819e-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzureRmSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="e819e-109">Esse comando habilita o status de execução automática de um supervisor chamado CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="e819e-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="e819e-110">OS</span><span class="sxs-lookup"><span data-stu-id="e819e-110">PARAMETERS</span></span>

### <span data-ttu-id="e819e-111">-Supervisorname</span><span class="sxs-lookup"><span data-stu-id="e819e-111">-AdvisorName</span></span>
<span data-ttu-id="e819e-112">Especifica o nome do supervisor para o qual esse cmdlet atualiza o status de execução automática.</span><span class="sxs-lookup"><span data-stu-id="e819e-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="e819e-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e819e-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="e819e-114">Especifica o valor para o qual esse cmdlet atualiza o status de execução automática.</span><span class="sxs-lookup"><span data-stu-id="e819e-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="e819e-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e819e-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e819e-116">Possibilita</span><span class="sxs-lookup"><span data-stu-id="e819e-116">Enabled</span></span>
- <span data-ttu-id="e819e-117">Ativo</span><span class="sxs-lookup"><span data-stu-id="e819e-117">Disabled</span></span>
- <span data-ttu-id="e819e-118">Assume</span><span class="sxs-lookup"><span data-stu-id="e819e-118">Default</span></span>

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

### <span data-ttu-id="e819e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e819e-119">-ResourceGroupName</span></span>
<span data-ttu-id="e819e-120">Especifica o nome do grupo de recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="e819e-120">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="e819e-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e819e-121">-ServerName</span></span>
<span data-ttu-id="e819e-122">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e819e-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e819e-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e819e-123">-Confirm</span></span>
<span data-ttu-id="e819e-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e819e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e819e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e819e-125">-WhatIf</span></span>
<span data-ttu-id="e819e-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e819e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e819e-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e819e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e819e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e819e-128">-DefaultProfile</span></span>
<span data-ttu-id="e819e-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e819e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e819e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e819e-130">CommonParameters</span></span>
<span data-ttu-id="e819e-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e819e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e819e-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e819e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e819e-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e819e-133">INPUTS</span></span>

## <span data-ttu-id="e819e-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e819e-134">OUTPUTS</span></span>

### <span data-ttu-id="e819e-135">Microsoft. Azure. Commands. Sql. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="e819e-135">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="e819e-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e819e-136">NOTES</span></span>
* <span data-ttu-id="e819e-137">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Server, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="e819e-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="e819e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e819e-138">RELATED LINKS</span></span>

[<span data-ttu-id="e819e-139">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="e819e-139">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="e819e-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e819e-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
