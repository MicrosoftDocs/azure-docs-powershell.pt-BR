---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 2e5e313fe35770e6841909e1f0718cfe3d9c8664
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603210"
---
# <span data-ttu-id="d527e-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d527e-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="d527e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d527e-102">SYNOPSIS</span></span>
<span data-ttu-id="d527e-103">Obtém uma política de backup geográfico do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d527e-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d527e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d527e-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d527e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d527e-105">DESCRIPTION</span></span>
<span data-ttu-id="d527e-106">O cmdlet **Get-AzureRmSqlDatabaseGeoBackupPolicy** Obtém a política de backup geográfico registrada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d527e-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="d527e-107">Este é um recurso de backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="d527e-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="d527e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d527e-108">EXAMPLES</span></span>

## <span data-ttu-id="d527e-109">OS</span><span class="sxs-lookup"><span data-stu-id="d527e-109">PARAMETERS</span></span>

### <span data-ttu-id="d527e-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d527e-110">-DatabaseName</span></span>
<span data-ttu-id="d527e-111">Especifica o nome do banco de dados para o qual esse cmdlet obtém a política de backup geográfico.</span><span class="sxs-lookup"><span data-stu-id="d527e-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d527e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d527e-112">-DefaultProfile</span></span>
<span data-ttu-id="d527e-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d527e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d527e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d527e-114">-ResourceGroupName</span></span>
<span data-ttu-id="d527e-115">Especifica o nome do grupo de recursos do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d527e-115">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d527e-116">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d527e-116">-ServerName</span></span>
<span data-ttu-id="d527e-117">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d527e-117">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d527e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d527e-118">CommonParameters</span></span>
<span data-ttu-id="d527e-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d527e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d527e-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d527e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d527e-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d527e-121">INPUTS</span></span>

### <span data-ttu-id="d527e-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d527e-122">None</span></span>
<span data-ttu-id="d527e-123">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d527e-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d527e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d527e-124">OUTPUTS</span></span>

## <span data-ttu-id="d527e-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d527e-125">NOTES</span></span>

## <span data-ttu-id="d527e-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d527e-126">RELATED LINKS</span></span>

[<span data-ttu-id="d527e-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d527e-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="d527e-128">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d527e-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
