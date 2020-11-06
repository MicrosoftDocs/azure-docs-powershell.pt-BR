---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 6ac39ae2daba5f97b9046f3860eb34d3bb0f03ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598792"
---
# <span data-ttu-id="08914-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="08914-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="08914-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08914-102">SYNOPSIS</span></span>
<span data-ttu-id="08914-103">Define uma política de backup geográfico do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="08914-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="08914-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08914-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08914-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08914-105">DESCRIPTION</span></span>
<span data-ttu-id="08914-106">O cmdlet **set-AzSqlDatabaseGeoBackupPolicy** define a política de backup geográfico registrada em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="08914-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="08914-107">Este é um recurso de backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="08914-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="08914-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08914-108">EXAMPLES</span></span>

## <span data-ttu-id="08914-109">OS</span><span class="sxs-lookup"><span data-stu-id="08914-109">PARAMETERS</span></span>

### <span data-ttu-id="08914-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="08914-110">-DatabaseName</span></span>
<span data-ttu-id="08914-111">Especifica o nome do banco de dados para o qual esse cmdlet define a política de backup geográfico.</span><span class="sxs-lookup"><span data-stu-id="08914-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="08914-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08914-112">-DefaultProfile</span></span>
<span data-ttu-id="08914-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="08914-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08914-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08914-114">-ResourceGroupName</span></span>
<span data-ttu-id="08914-115">Especifica o nome do grupo de recursos do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="08914-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="08914-116">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="08914-116">-ServerName</span></span>
<span data-ttu-id="08914-117">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="08914-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="08914-118">-Estado</span><span class="sxs-lookup"><span data-stu-id="08914-118">-State</span></span>
<span data-ttu-id="08914-119">Especifica o estado da política de backup geográfico.</span><span class="sxs-lookup"><span data-stu-id="08914-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="08914-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="08914-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="08914-121">Possibilita</span><span class="sxs-lookup"><span data-stu-id="08914-121">Enabled</span></span> 
- <span data-ttu-id="08914-122">Ativo</span><span class="sxs-lookup"><span data-stu-id="08914-122">Disabled</span></span>

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

### <span data-ttu-id="08914-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="08914-123">-Confirm</span></span>
<span data-ttu-id="08914-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08914-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08914-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08914-125">-WhatIf</span></span>
<span data-ttu-id="08914-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="08914-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08914-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08914-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08914-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08914-128">CommonParameters</span></span>
<span data-ttu-id="08914-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08914-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08914-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08914-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08914-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08914-131">INPUTS</span></span>

### <span data-ttu-id="08914-132">System. String</span><span class="sxs-lookup"><span data-stu-id="08914-132">System.String</span></span>

## <span data-ttu-id="08914-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08914-133">OUTPUTS</span></span>

### <span data-ttu-id="08914-134">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="08914-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="08914-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08914-135">NOTES</span></span>

## <span data-ttu-id="08914-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08914-136">RELATED LINKS</span></span>

[<span data-ttu-id="08914-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="08914-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="08914-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="08914-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

