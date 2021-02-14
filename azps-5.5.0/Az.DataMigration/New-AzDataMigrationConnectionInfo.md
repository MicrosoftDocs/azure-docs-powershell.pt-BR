---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: e902785745ab22ab9bc1386fc2c6a2f9dd416b79
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110985"
---
# <span data-ttu-id="df719-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="df719-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="df719-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df719-102">SYNOPSIS</span></span>
<span data-ttu-id="df719-103">Cria um novo objeto Informações de Conexão especificando o tipo e o nome do servidor para conexão.</span><span class="sxs-lookup"><span data-stu-id="df719-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="df719-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df719-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df719-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="df719-105">DESCRIPTION</span></span>
<span data-ttu-id="df719-106">O New-AzDataMigrationConnectionInfo cmdlet cria um novo objeto Informações de Conexão especificando o tipo de servidor para conexão.</span><span class="sxs-lookup"><span data-stu-id="df719-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="df719-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="df719-107">EXAMPLES</span></span>

### <span data-ttu-id="df719-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df719-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="df719-109">O exemplo anterior cria um novo objeto Informações de Conexão que fornece SQL como parâmetro ServerType.</span><span class="sxs-lookup"><span data-stu-id="df719-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="df719-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df719-110">PARAMETERS</span></span>

### <span data-ttu-id="df719-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df719-111">-DefaultProfile</span></span>
<span data-ttu-id="df719-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="df719-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df719-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="df719-113">-ServerType</span></span>
<span data-ttu-id="df719-114">Número que descreve o tipo de servidor ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="df719-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="df719-115">Atualmente, os valores com suporte são SQL para SQL Server, Instância Gerenciada do Azure SQL, MongoDb, SqlDb e Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="df719-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

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

### <span data-ttu-id="df719-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df719-116">CommonParameters</span></span>
<span data-ttu-id="df719-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df719-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df719-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df719-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df719-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="df719-119">INPUTS</span></span>

### <span data-ttu-id="df719-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="df719-120">None</span></span>

## <span data-ttu-id="df719-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="df719-121">OUTPUTS</span></span>

### <span data-ttu-id="df719-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="df719-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="df719-123">Notas</span><span class="sxs-lookup"><span data-stu-id="df719-123">NOTES</span></span>

## <span data-ttu-id="df719-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df719-124">RELATED LINKS</span></span>
