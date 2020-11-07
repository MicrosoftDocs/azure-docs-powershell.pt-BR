---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: d69d6c2976e71183fed07e2c18adc730d8ea6e61
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941546"
---
# <span data-ttu-id="59263-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="59263-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="59263-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59263-102">SYNOPSIS</span></span>
<span data-ttu-id="59263-103">Obtém uma política de backup geográfico do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="59263-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="59263-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59263-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59263-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59263-105">DESCRIPTION</span></span>
<span data-ttu-id="59263-106">O cmdlet **Get-AzSqlDatabaseGeoBackupPolicy** Obtém a política de backup geográfico registrada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="59263-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="59263-107">Este é um recurso de backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="59263-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="59263-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59263-108">EXAMPLES</span></span>

## <span data-ttu-id="59263-109">OS</span><span class="sxs-lookup"><span data-stu-id="59263-109">PARAMETERS</span></span>

### <span data-ttu-id="59263-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59263-110">-DatabaseName</span></span>
<span data-ttu-id="59263-111">Especifica o nome do banco de dados para o qual esse cmdlet obtém a política de backup geográfico.</span><span class="sxs-lookup"><span data-stu-id="59263-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59263-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59263-112">-DefaultProfile</span></span>
<span data-ttu-id="59263-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="59263-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59263-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59263-114">-ResourceGroupName</span></span>
<span data-ttu-id="59263-115">Especifica o nome do grupo de recursos do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="59263-115">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59263-116">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="59263-116">-ServerName</span></span>
<span data-ttu-id="59263-117">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="59263-117">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59263-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59263-118">CommonParameters</span></span>
<span data-ttu-id="59263-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59263-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59263-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59263-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59263-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59263-121">INPUTS</span></span>

### <span data-ttu-id="59263-122">System. String</span><span class="sxs-lookup"><span data-stu-id="59263-122">System.String</span></span>

## <span data-ttu-id="59263-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59263-123">OUTPUTS</span></span>

### <span data-ttu-id="59263-124">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="59263-124">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="59263-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59263-125">NOTES</span></span>

## <span data-ttu-id="59263-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59263-126">RELATED LINKS</span></span>

[<span data-ttu-id="59263-127">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="59263-127">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="59263-128">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="59263-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
