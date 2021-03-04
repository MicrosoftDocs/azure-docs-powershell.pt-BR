---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: b30f9fd4b29a1be064a9e0925e39faa71485b58f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887208"
---
# <span data-ttu-id="af970-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="af970-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="af970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af970-102">SYNOPSIS</span></span>
<span data-ttu-id="af970-103">Cria o objeto FileShare para o Serviço de Migração de Banco de Dados do Azure, que especifica o compartilhamento de rede local para o qual fazer os backups do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="af970-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="af970-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="af970-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af970-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="af970-105">DESCRIPTION</span></span>
<span data-ttu-id="af970-106">O New-AzDataMigrationFileShare cmdlet cria o objeto FileShare que especifica o compartilhamento de rede local para o que o Serviço de Migração de Banco de Dados do Azure pode fazer backups do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="af970-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="af970-107">A conta de serviço que executa a SQL Server de origem deve ter privilégios de gravação neste compartilhamento de rede.</span><span class="sxs-lookup"><span data-stu-id="af970-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="af970-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af970-108">EXAMPLES</span></span>

### <span data-ttu-id="af970-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af970-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="af970-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="af970-110">PARAMETERS</span></span>

### <span data-ttu-id="af970-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="af970-111">-Credential</span></span>
<span data-ttu-id="af970-112">Credenciais para acessar o compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="af970-112">Credentials to access the file share.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af970-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af970-113">-DefaultProfile</span></span>
<span data-ttu-id="af970-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af970-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af970-115">-Path</span><span class="sxs-lookup"><span data-stu-id="af970-115">-Path</span></span>
<span data-ttu-id="af970-116">Caminho de compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="af970-116">File share path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af970-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af970-117">CommonParameters</span></span>
<span data-ttu-id="af970-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af970-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af970-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af970-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af970-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af970-120">INPUTS</span></span>

### <span data-ttu-id="af970-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="af970-121">None</span></span>

## <span data-ttu-id="af970-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="af970-122">OUTPUTS</span></span>

### <span data-ttu-id="af970-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="af970-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="af970-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="af970-124">NOTES</span></span>

## <span data-ttu-id="af970-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af970-125">RELATED LINKS</span></span>
