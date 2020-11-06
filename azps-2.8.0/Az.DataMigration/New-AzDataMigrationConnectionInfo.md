---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: 871b6c09832e4b857a616c93cc33102f2dd0ad8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596783"
---
# <span data-ttu-id="edfde-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="edfde-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="edfde-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="edfde-102">SYNOPSIS</span></span>
<span data-ttu-id="edfde-103">Cria um novo objeto de informações de conexão especificando o tipo e o nome do servidor para a conexão.</span><span class="sxs-lookup"><span data-stu-id="edfde-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="edfde-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edfde-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="edfde-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="edfde-105">DESCRIPTION</span></span>
<span data-ttu-id="edfde-106">O cmdlet New-AzDataMigrationConnectionInfo cria um objeto de informações de conexão novo especificando o tipo de servidor para conexão.</span><span class="sxs-lookup"><span data-stu-id="edfde-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="edfde-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="edfde-107">EXAMPLES</span></span>

### <span data-ttu-id="edfde-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="edfde-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="edfde-109">O exemplo anterior cria um novo objeto de informações de conexão fornecendo SQL como parâmetro ServerType.</span><span class="sxs-lookup"><span data-stu-id="edfde-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="edfde-110">OS</span><span class="sxs-lookup"><span data-stu-id="edfde-110">PARAMETERS</span></span>

### <span data-ttu-id="edfde-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edfde-111">-DefaultProfile</span></span>
<span data-ttu-id="edfde-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="edfde-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edfde-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="edfde-113">-ServerType</span></span>
<span data-ttu-id="edfde-114">Enum que descreve o tipo de servidor ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="edfde-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="edfde-115">Os valores atualmente com suporte são SQL Server, SQL Server, instância gerenciada SQL do Azure, Azure, CosmosDb e banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="edfde-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL, MongoDb, SQLMI

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfde-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edfde-116">CommonParameters</span></span>
<span data-ttu-id="edfde-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edfde-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edfde-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edfde-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edfde-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="edfde-119">INPUTS</span></span>

### <span data-ttu-id="edfde-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="edfde-120">None</span></span>

## <span data-ttu-id="edfde-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="edfde-121">OUTPUTS</span></span>

### <span data-ttu-id="edfde-122">Microsoft. Azure. Management. datamigration. Models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="edfde-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="edfde-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="edfde-123">NOTES</span></span>

## <span data-ttu-id="edfde-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="edfde-124">RELATED LINKS</span></span>
