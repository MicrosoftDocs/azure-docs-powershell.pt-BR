---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: c04a79a54e42c64fe897a419565e4816964879b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610910"
---
# <span data-ttu-id="e410b-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="e410b-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="e410b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e410b-102">SYNOPSIS</span></span>
<span data-ttu-id="e410b-103">Cria o objeto DatabaseInfo para o serviço de migração de banco de dados do Azure, que especifica a origem do banco de dados para migração.</span><span class="sxs-lookup"><span data-stu-id="e410b-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e410b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e410b-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e410b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e410b-105">DESCRIPTION</span></span>
<span data-ttu-id="e410b-106">O cmdlet New-AzureRmDataMigrationDatabaseInfo cria o objeto DatabaseInfo que especifica a instância do banco de dados de origem a ser migrada.</span><span class="sxs-lookup"><span data-stu-id="e410b-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="e410b-107">O nome do banco de dados é usado como parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="e410b-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="e410b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e410b-108">EXAMPLES</span></span>

### <span data-ttu-id="e410b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e410b-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="e410b-110">O exemplo anterior cria um novo objeto DatabaseInfo para o banco de dados de origem **AdventureWorks2016**.</span><span class="sxs-lookup"><span data-stu-id="e410b-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="e410b-111">Esse script pressupõe que você já esteja conectado à sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="e410b-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="e410b-112">Você pode confirmar seu status de logon usando o cmdlet Get-AzureSubscription.</span><span class="sxs-lookup"><span data-stu-id="e410b-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="e410b-113">OS</span><span class="sxs-lookup"><span data-stu-id="e410b-113">PARAMETERS</span></span>

### <span data-ttu-id="e410b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e410b-114">-DefaultProfile</span></span>
<span data-ttu-id="e410b-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e410b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e410b-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e410b-116">-SourceDatabaseName</span></span>
<span data-ttu-id="e410b-117">Nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="e410b-117">Source Database Name.</span></span>

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

### <span data-ttu-id="e410b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e410b-118">CommonParameters</span></span>
<span data-ttu-id="e410b-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e410b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e410b-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e410b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e410b-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e410b-121">INPUTS</span></span>

### <span data-ttu-id="e410b-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e410b-122">None</span></span>

## <span data-ttu-id="e410b-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e410b-123">OUTPUTS</span></span>

### <span data-ttu-id="e410b-124">Microsoft. Azure. Management. datamigration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="e410b-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="e410b-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e410b-125">NOTES</span></span>

## <span data-ttu-id="e410b-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e410b-126">RELATED LINKS</span></span>
