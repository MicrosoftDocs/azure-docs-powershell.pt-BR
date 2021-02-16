---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127026"
---
# <span data-ttu-id="6f798-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="6f798-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="6f798-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f798-102">SYNOPSIS</span></span>
<span data-ttu-id="6f798-103">Cria o objeto DatabaseInfo para o Serviço de Migração de Banco de Dados do Azure, que especifica a fonte de banco de dados para migração.</span><span class="sxs-lookup"><span data-stu-id="6f798-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="6f798-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f798-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f798-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f798-105">DESCRIPTION</span></span>
<span data-ttu-id="6f798-106">O New-AzDataMigrationDatabaseInfo cmdlet cria o objeto DatabaseInfo que especifica a instância do banco de dados de origem a ser migrada.</span><span class="sxs-lookup"><span data-stu-id="6f798-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="6f798-107">O nome do banco de dados é chamado de parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="6f798-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="6f798-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6f798-108">EXAMPLES</span></span>

### <span data-ttu-id="6f798-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f798-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="6f798-110">O exemplo anterior cria um novo objeto DatabaseInfo para o banco de dados de origem **AdventureWorks2016.**</span><span class="sxs-lookup"><span data-stu-id="6f798-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="6f798-111">Este script pressuposição de que você já está conectado à sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="6f798-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="6f798-112">Você pode confirmar seu status de logon usando o cmdlet Get-AzSubscription usuário.</span><span class="sxs-lookup"><span data-stu-id="6f798-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="6f798-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f798-113">PARAMETERS</span></span>

### <span data-ttu-id="6f798-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f798-114">-DefaultProfile</span></span>
<span data-ttu-id="6f798-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6f798-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f798-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6f798-116">-SourceDatabaseName</span></span>
<span data-ttu-id="6f798-117">Nome do Banco de Dados de Origem.</span><span class="sxs-lookup"><span data-stu-id="6f798-117">Source Database Name.</span></span>

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

### <span data-ttu-id="6f798-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f798-118">CommonParameters</span></span>
<span data-ttu-id="6f798-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f798-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f798-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f798-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f798-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="6f798-121">INPUTS</span></span>

### <span data-ttu-id="6f798-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6f798-122">None</span></span>

## <span data-ttu-id="6f798-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="6f798-123">OUTPUTS</span></span>

### <span data-ttu-id="6f798-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="6f798-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="6f798-125">Notas</span><span class="sxs-lookup"><span data-stu-id="6f798-125">NOTES</span></span>

## <span data-ttu-id="6f798-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f798-126">RELATED LINKS</span></span>
