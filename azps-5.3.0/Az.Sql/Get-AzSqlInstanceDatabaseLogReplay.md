---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428701"
---
# <span data-ttu-id="39e06-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="39e06-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="39e06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39e06-102">SYNOPSIS</span></span>
<span data-ttu-id="39e06-103">Obtém o status do serviço de repetição de log.</span><span class="sxs-lookup"><span data-stu-id="39e06-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="39e06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39e06-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39e06-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39e06-105">DESCRIPTION</span></span>
<span data-ttu-id="39e06-106">O cmdlet **Get-AzSqlInstanceDatabaseLogReplay** Obtém o status do serviço de repetição de log no banco de dados fornecido.</span><span class="sxs-lookup"><span data-stu-id="39e06-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="39e06-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39e06-107">EXAMPLES</span></span>

### <span data-ttu-id="39e06-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="39e06-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="39e06-109">Esse comando receberá o status do serviço de reprodução de log em um determinado banco de dados.</span><span class="sxs-lookup"><span data-stu-id="39e06-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="39e06-110">OS</span><span class="sxs-lookup"><span data-stu-id="39e06-110">PARAMETERS</span></span>

### <span data-ttu-id="39e06-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e06-111">-DefaultProfile</span></span>
<span data-ttu-id="39e06-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39e06-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39e06-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="39e06-113">-InstanceName</span></span>
<span data-ttu-id="39e06-114">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="39e06-114">The name of the instance.</span></span>

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

### <span data-ttu-id="39e06-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="39e06-115">-Name</span></span>
<span data-ttu-id="39e06-116">O nome do banco de dados de instância a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="39e06-116">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="39e06-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39e06-117">-ResourceGroupName</span></span>
<span data-ttu-id="39e06-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="39e06-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="39e06-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e06-119">CommonParameters</span></span>
<span data-ttu-id="39e06-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39e06-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e06-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39e06-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e06-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39e06-122">INPUTS</span></span>

### <span data-ttu-id="39e06-123">System. String</span><span class="sxs-lookup"><span data-stu-id="39e06-123">System.String</span></span>

## <span data-ttu-id="39e06-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39e06-124">OUTPUTS</span></span>

### <span data-ttu-id="39e06-125">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="39e06-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="39e06-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39e06-126">NOTES</span></span>

## <span data-ttu-id="39e06-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39e06-127">RELATED LINKS</span></span>
