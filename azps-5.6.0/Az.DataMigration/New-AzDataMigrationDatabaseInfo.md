---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: 2152835d997532b490a6be16bf329831071f2f87
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887214"
---
# <span data-ttu-id="b4cb0-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="b4cb0-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="b4cb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="b4cb0-103">Cria o objeto DatabaseInfo para o Serviço de Migração de Banco de Dados do Azure, que especifica a origem do banco de dados para migração.</span><span class="sxs-lookup"><span data-stu-id="b4cb0-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="b4cb0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b4cb0-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4cb0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b4cb0-105">DESCRIPTION</span></span>
<span data-ttu-id="b4cb0-106">O New-AzDataMigrationDatabaseInfo cmdlet cria o objeto DatabaseInfo que especifica a instância do banco de dados de origem a ser migrada.</span><span class="sxs-lookup"><span data-stu-id="b4cb0-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="b4cb0-107">O nome do banco de dados é tomado como parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="b4cb0-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="b4cb0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4cb0-108">EXAMPLES</span></span>

### <span data-ttu-id="b4cb0-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4cb0-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="b4cb0-110">O exemplo anterior cria um novo objeto DatabaseInfo para o banco de dados de origem **AdventureWorks2016**.</span><span class="sxs-lookup"><span data-stu-id="b4cb0-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="b4cb0-111">Este script supõe que você já está conectado à sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4cb0-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="b4cb0-112">Você pode confirmar seu status de logon usando o cmdlet Get-AzSubscription usuário.</span><span class="sxs-lookup"><span data-stu-id="b4cb0-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="b4cb0-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b4cb0-113">PARAMETERS</span></span>

### <span data-ttu-id="b4cb0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4cb0-114">-DefaultProfile</span></span>
<span data-ttu-id="b4cb0-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b4cb0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4cb0-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b4cb0-116">-SourceDatabaseName</span></span>
<span data-ttu-id="b4cb0-117">Nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="b4cb0-117">Source Database Name.</span></span>

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

### <span data-ttu-id="b4cb0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4cb0-118">CommonParameters</span></span>
<span data-ttu-id="b4cb0-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4cb0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4cb0-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4cb0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4cb0-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4cb0-121">INPUTS</span></span>

### <span data-ttu-id="b4cb0-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b4cb0-122">None</span></span>

## <span data-ttu-id="b4cb0-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b4cb0-123">OUTPUTS</span></span>

### <span data-ttu-id="b4cb0-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="b4cb0-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="b4cb0-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="b4cb0-125">NOTES</span></span>

## <span data-ttu-id="b4cb0-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4cb0-126">RELATED LINKS</span></span>
