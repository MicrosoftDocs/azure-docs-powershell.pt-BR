---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7f2589c665bd24fdb2d017cd8cfd4ca055e3e429
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891584"
---
# <span data-ttu-id="0bf96-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="0bf96-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="0bf96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bf96-102">SYNOPSIS</span></span>
<span data-ttu-id="0bf96-103">Obtém o status do serviço de Repetição de Log.</span><span class="sxs-lookup"><span data-stu-id="0bf96-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="0bf96-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0bf96-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bf96-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0bf96-105">DESCRIPTION</span></span>
<span data-ttu-id="0bf96-106">O cmdlet **Get-AzSqlInstanceDatabaseLogReplay** obtém o status do serviço de Repetição de Log no banco de dados determinado.</span><span class="sxs-lookup"><span data-stu-id="0bf96-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="0bf96-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0bf96-107">EXAMPLES</span></span>

### <span data-ttu-id="0bf96-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0bf96-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="0bf96-109">Este comando receberá o status do serviço de repetição de log no banco de dados determinado.</span><span class="sxs-lookup"><span data-stu-id="0bf96-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="0bf96-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0bf96-110">PARAMETERS</span></span>

### <span data-ttu-id="0bf96-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bf96-111">-DefaultProfile</span></span>
<span data-ttu-id="0bf96-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0bf96-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bf96-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0bf96-113">-InstanceName</span></span>
<span data-ttu-id="0bf96-114">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="0bf96-114">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bf96-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0bf96-115">-Name</span></span>
<span data-ttu-id="0bf96-116">O nome do banco de dados de instância a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="0bf96-116">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bf96-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bf96-117">-ResourceGroupName</span></span>
<span data-ttu-id="0bf96-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0bf96-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bf96-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bf96-119">CommonParameters</span></span>
<span data-ttu-id="0bf96-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bf96-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bf96-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bf96-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bf96-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0bf96-122">INPUTS</span></span>

### <span data-ttu-id="0bf96-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0bf96-123">System.String</span></span>

## <span data-ttu-id="0bf96-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0bf96-124">OUTPUTS</span></span>

### <span data-ttu-id="0bf96-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="0bf96-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="0bf96-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="0bf96-126">NOTES</span></span>

## <span data-ttu-id="0bf96-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bf96-127">RELATED LINKS</span></span>
