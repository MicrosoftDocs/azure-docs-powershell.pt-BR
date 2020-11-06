---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationdatabaseinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: 3b0729b07667e634f060293bd8593ed237606460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610401"
---
# <span data-ttu-id="43752-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="43752-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="43752-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43752-102">SYNOPSIS</span></span>
<span data-ttu-id="43752-103">Cria o objeto DatabaseInfo para o serviço de migração de banco de dados do Azure, que especifica a origem do banco de dados para migração.</span><span class="sxs-lookup"><span data-stu-id="43752-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43752-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43752-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="43752-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43752-105">DESCRIPTION</span></span>
<span data-ttu-id="43752-106">O cmdlet New-AzureRmDataMigrationDatabaseInfo cria o objeto DatabaseInfo que especifica a instância do banco de dados de origem a ser migrada.</span><span class="sxs-lookup"><span data-stu-id="43752-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="43752-107">O nome do banco de dados é usado como parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="43752-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="43752-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43752-108">EXAMPLES</span></span>

### <span data-ttu-id="43752-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="43752-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="43752-110">O exemplo anterior cria um novo objeto DatabaseInfo para o banco de dados de origem **AdventureWorks2016**.</span><span class="sxs-lookup"><span data-stu-id="43752-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>

<span data-ttu-id="43752-111">Esse script pressupõe que você já esteja conectado à sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="43752-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="43752-112">Você pode confirmar seu status de logon usando o cmdlet Get-AzureSubscription.</span><span class="sxs-lookup"><span data-stu-id="43752-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="43752-113">OS</span><span class="sxs-lookup"><span data-stu-id="43752-113">PARAMETERS</span></span>

### <span data-ttu-id="43752-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43752-114">-DefaultProfile</span></span>
<span data-ttu-id="43752-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43752-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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
### <span data-ttu-id="43752-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="43752-116">-Confirm</span></span>
<span data-ttu-id="43752-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43752-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43752-118">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="43752-118">-SourceDatabaseName</span></span>
<span data-ttu-id="43752-119">Nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="43752-119">Source Database Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43752-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43752-120">-WhatIf</span></span>
<span data-ttu-id="43752-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="43752-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43752-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="43752-122">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="43752-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43752-123">INPUTS</span></span>

### <span data-ttu-id="43752-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="43752-124">None</span></span>


## <span data-ttu-id="43752-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43752-125">OUTPUTS</span></span>

### <span data-ttu-id="43752-126">Microsoft. Azure. Management. datamigration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="43752-126">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>


## <span data-ttu-id="43752-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43752-127">NOTES</span></span>

## <span data-ttu-id="43752-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43752-128">RELATED LINKS</span></span>


