---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 18ae68a4ecf0a2511f992e42a202468193022d6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890937"
---
# <span data-ttu-id="7924a-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7924a-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="7924a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7924a-102">SYNOPSIS</span></span>
<span data-ttu-id="7924a-103">Define uma política de backup geo-geográfica do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7924a-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="7924a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7924a-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7924a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7924a-105">DESCRIPTION</span></span>
<span data-ttu-id="7924a-106">O cmdlet **Set-AzSqlDatabaseGeoBackupPolicy** define a política de backup geográfica registrada em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7924a-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="7924a-107">Este é um recurso de Backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="7924a-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="7924a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7924a-108">EXAMPLES</span></span>

## <span data-ttu-id="7924a-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7924a-109">PARAMETERS</span></span>

### <span data-ttu-id="7924a-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7924a-110">-DatabaseName</span></span>
<span data-ttu-id="7924a-111">Especifica o nome do banco de dados para o qual este cmdlet define a política de backup geo.</span><span class="sxs-lookup"><span data-stu-id="7924a-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="7924a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7924a-112">-DefaultProfile</span></span>
<span data-ttu-id="7924a-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7924a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7924a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7924a-114">-ResourceGroupName</span></span>
<span data-ttu-id="7924a-115">Especifica o nome do grupo de recursos do servidor que contém esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7924a-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="7924a-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7924a-116">-ServerName</span></span>
<span data-ttu-id="7924a-117">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7924a-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="7924a-118">-State</span><span class="sxs-lookup"><span data-stu-id="7924a-118">-State</span></span>
<span data-ttu-id="7924a-119">Especifica o estado da política de backup geo.</span><span class="sxs-lookup"><span data-stu-id="7924a-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="7924a-120">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7924a-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7924a-121">Habilitado</span><span class="sxs-lookup"><span data-stu-id="7924a-121">Enabled</span></span> 
- <span data-ttu-id="7924a-122">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="7924a-122">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel+GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7924a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7924a-123">-Confirm</span></span>
<span data-ttu-id="7924a-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7924a-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7924a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7924a-125">-WhatIf</span></span>
<span data-ttu-id="7924a-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7924a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7924a-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7924a-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7924a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7924a-128">CommonParameters</span></span>
<span data-ttu-id="7924a-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7924a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7924a-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7924a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7924a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7924a-131">INPUTS</span></span>

### <span data-ttu-id="7924a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7924a-132">System.String</span></span>

## <span data-ttu-id="7924a-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7924a-133">OUTPUTS</span></span>

### <span data-ttu-id="7924a-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7924a-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="7924a-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="7924a-135">NOTES</span></span>

## <span data-ttu-id="7924a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7924a-136">RELATED LINKS</span></span>

[<span data-ttu-id="7924a-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7924a-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="7924a-138">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="7924a-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

