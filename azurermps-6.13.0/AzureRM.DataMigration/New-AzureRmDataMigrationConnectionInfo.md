---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: 77559f5858c26d665d062f822a5c65258625bb14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602952"
---
# <span data-ttu-id="6795f-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="6795f-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="6795f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6795f-102">SYNOPSIS</span></span>
<span data-ttu-id="6795f-103">Cria um novo objeto de informações de conexão especificando o tipo e o nome do servidor para a conexão.</span><span class="sxs-lookup"><span data-stu-id="6795f-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6795f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6795f-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6795f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6795f-105">DESCRIPTION</span></span>
<span data-ttu-id="6795f-106">O cmdlet New-AzureRmDataMigrationConnectionInfo cria um objeto de informações de conexão novo especificando o tipo de servidor para conexão.</span><span class="sxs-lookup"><span data-stu-id="6795f-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="6795f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6795f-107">EXAMPLES</span></span>

### <span data-ttu-id="6795f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6795f-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="6795f-109">O exemplo anterior cria um novo objeto de informações de conexão fornecendo SQL como parâmetro ServerType.</span><span class="sxs-lookup"><span data-stu-id="6795f-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="6795f-110">OS</span><span class="sxs-lookup"><span data-stu-id="6795f-110">PARAMETERS</span></span>

### <span data-ttu-id="6795f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6795f-111">-DefaultProfile</span></span>
<span data-ttu-id="6795f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6795f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6795f-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="6795f-113">-ServerType</span></span>
<span data-ttu-id="6795f-114">Enum que descreve o tipo de servidor ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="6795f-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="6795f-115">Os valores atualmente com suporte são SQL Server, SQL Server, Azure SQL Managed e Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="6795f-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6795f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6795f-116">CommonParameters</span></span>
<span data-ttu-id="6795f-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6795f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6795f-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6795f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6795f-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6795f-119">INPUTS</span></span>

### <span data-ttu-id="6795f-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6795f-120">None</span></span>

## <span data-ttu-id="6795f-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6795f-121">OUTPUTS</span></span>

### <span data-ttu-id="6795f-122">Microsoft. Azure. Management. datamigration. Models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="6795f-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="6795f-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6795f-123">NOTES</span></span>

## <span data-ttu-id="6795f-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6795f-124">RELATED LINKS</span></span>
