---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
ms.openlocfilehash: b34665f9402186a1e07671e614d91fee59f565d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433257"
---
# <span data-ttu-id="f5e49-101">New-AzureRmDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="f5e49-101">New-AzureRmDataMigrationFileShare</span></span>

## <span data-ttu-id="f5e49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5e49-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e49-103">Cria o objeto FileShare para o serviço de migração de banco de dados do Azure, que especifica o compartilhamento de rede local para levar os backups do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="f5e49-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5e49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5e49-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5e49-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5e49-105">DESCRIPTION</span></span>
<span data-ttu-id="f5e49-106">O cmdlet New-AzureRmDataMigrationFileShare cria o objeto FileShare que especifica o compartilhamento de rede local que o serviço de migração de banco de dados do Azure pode fazer backups de banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="f5e49-106">The New-AzureRmDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="f5e49-107">A conta de serviço que executa a instância do SQL Server de origem deve ter privilégios de gravação nesse compartilhamento de rede.</span><span class="sxs-lookup"><span data-stu-id="f5e49-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="f5e49-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5e49-108">EXAMPLES</span></span>

### <span data-ttu-id="f5e49-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f5e49-109">Example 1</span></span>
```
PS C:\> New-AzureRmDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="f5e49-110">OS</span><span class="sxs-lookup"><span data-stu-id="f5e49-110">PARAMETERS</span></span>

### <span data-ttu-id="f5e49-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="f5e49-111">-Credential</span></span>
<span data-ttu-id="f5e49-112">Credenciais para acessar o compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f5e49-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="f5e49-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e49-113">-DefaultProfile</span></span>
<span data-ttu-id="f5e49-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e49-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5e49-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="f5e49-115">-Path</span></span>
<span data-ttu-id="f5e49-116">Caminho de compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f5e49-116">File share path.</span></span>

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

### <span data-ttu-id="f5e49-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e49-117">CommonParameters</span></span>
<span data-ttu-id="f5e49-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5e49-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e49-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5e49-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e49-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5e49-120">INPUTS</span></span>

### <span data-ttu-id="f5e49-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f5e49-121">None</span></span>

## <span data-ttu-id="f5e49-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5e49-122">OUTPUTS</span></span>

### <span data-ttu-id="f5e49-123">Microsoft. Azure. Management. datamigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="f5e49-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="f5e49-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5e49-124">NOTES</span></span>

## <span data-ttu-id="f5e49-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5e49-125">RELATED LINKS</span></span>
