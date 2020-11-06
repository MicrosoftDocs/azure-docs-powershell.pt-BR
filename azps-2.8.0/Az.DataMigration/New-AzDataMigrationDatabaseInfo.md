---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: f1feead56c25b76890edd0fe183e65211294cf87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596778"
---
# <span data-ttu-id="8dcfb-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="8dcfb-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="8dcfb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8dcfb-102">SYNOPSIS</span></span>
<span data-ttu-id="8dcfb-103">Cria o objeto DatabaseInfo para o serviço de migração de banco de dados do Azure, que especifica a origem do banco de dados para migração.</span><span class="sxs-lookup"><span data-stu-id="8dcfb-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="8dcfb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8dcfb-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8dcfb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8dcfb-105">DESCRIPTION</span></span>
<span data-ttu-id="8dcfb-106">O cmdlet New-AzDataMigrationDatabaseInfo cria o objeto DatabaseInfo que especifica a instância do banco de dados de origem a ser migrada.</span><span class="sxs-lookup"><span data-stu-id="8dcfb-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="8dcfb-107">O nome do banco de dados é usado como parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="8dcfb-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="8dcfb-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8dcfb-108">EXAMPLES</span></span>

### <span data-ttu-id="8dcfb-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8dcfb-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="8dcfb-110">O exemplo anterior cria um novo objeto DatabaseInfo para o banco de dados de origem **AdventureWorks2016**.</span><span class="sxs-lookup"><span data-stu-id="8dcfb-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="8dcfb-111">Esse script pressupõe que você já esteja conectado à sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="8dcfb-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="8dcfb-112">Você pode confirmar seu status de logon usando o cmdlet Get-AzSubscription.</span><span class="sxs-lookup"><span data-stu-id="8dcfb-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="8dcfb-113">OS</span><span class="sxs-lookup"><span data-stu-id="8dcfb-113">PARAMETERS</span></span>

### <span data-ttu-id="8dcfb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dcfb-114">-DefaultProfile</span></span>
<span data-ttu-id="8dcfb-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8dcfb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dcfb-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8dcfb-116">-SourceDatabaseName</span></span>
<span data-ttu-id="8dcfb-117">Nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="8dcfb-117">Source Database Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dcfb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dcfb-118">CommonParameters</span></span>
<span data-ttu-id="8dcfb-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dcfb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dcfb-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dcfb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dcfb-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8dcfb-121">INPUTS</span></span>

### <span data-ttu-id="8dcfb-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8dcfb-122">None</span></span>

## <span data-ttu-id="8dcfb-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8dcfb-123">OUTPUTS</span></span>

### <span data-ttu-id="8dcfb-124">Microsoft. Azure. Management. datamigration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="8dcfb-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="8dcfb-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8dcfb-125">NOTES</span></span>

## <span data-ttu-id="8dcfb-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8dcfb-126">RELATED LINKS</span></span>
