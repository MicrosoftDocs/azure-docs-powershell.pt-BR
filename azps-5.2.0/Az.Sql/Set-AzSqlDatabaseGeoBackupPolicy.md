---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 07836205ec7311eadf7e48dd79b322d00670f337
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264229"
---
# <span data-ttu-id="e82d7-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e82d7-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="e82d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e82d7-102">SYNOPSIS</span></span>
<span data-ttu-id="e82d7-103">Define uma política de backup geográfico do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e82d7-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="e82d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e82d7-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e82d7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e82d7-105">DESCRIPTION</span></span>
<span data-ttu-id="e82d7-106">O cmdlet **set-AzSqlDatabaseGeoBackupPolicy** define a política de backup geográfico registrada em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e82d7-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="e82d7-107">Este é um recurso de backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="e82d7-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="e82d7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e82d7-108">EXAMPLES</span></span>

## <span data-ttu-id="e82d7-109">OS</span><span class="sxs-lookup"><span data-stu-id="e82d7-109">PARAMETERS</span></span>

### <span data-ttu-id="e82d7-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e82d7-110">-DatabaseName</span></span>
<span data-ttu-id="e82d7-111">Especifica o nome do banco de dados para o qual esse cmdlet define a política de backup geográfico.</span><span class="sxs-lookup"><span data-stu-id="e82d7-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="e82d7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e82d7-112">-DefaultProfile</span></span>
<span data-ttu-id="e82d7-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e82d7-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e82d7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e82d7-114">-ResourceGroupName</span></span>
<span data-ttu-id="e82d7-115">Especifica o nome do grupo de recursos do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e82d7-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="e82d7-116">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e82d7-116">-ServerName</span></span>
<span data-ttu-id="e82d7-117">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e82d7-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="e82d7-118">-Estado</span><span class="sxs-lookup"><span data-stu-id="e82d7-118">-State</span></span>
<span data-ttu-id="e82d7-119">Especifica o estado da política de backup geográfico.</span><span class="sxs-lookup"><span data-stu-id="e82d7-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="e82d7-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e82d7-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e82d7-121">Possibilita</span><span class="sxs-lookup"><span data-stu-id="e82d7-121">Enabled</span></span> 
- <span data-ttu-id="e82d7-122">Ativo</span><span class="sxs-lookup"><span data-stu-id="e82d7-122">Disabled</span></span>

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

### <span data-ttu-id="e82d7-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e82d7-123">-Confirm</span></span>
<span data-ttu-id="e82d7-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e82d7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e82d7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e82d7-125">-WhatIf</span></span>
<span data-ttu-id="e82d7-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e82d7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e82d7-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e82d7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e82d7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e82d7-128">CommonParameters</span></span>
<span data-ttu-id="e82d7-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e82d7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e82d7-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e82d7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e82d7-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e82d7-131">INPUTS</span></span>

### <span data-ttu-id="e82d7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e82d7-132">System.String</span></span>

## <span data-ttu-id="e82d7-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e82d7-133">OUTPUTS</span></span>

### <span data-ttu-id="e82d7-134">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e82d7-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="e82d7-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e82d7-135">NOTES</span></span>

## <span data-ttu-id="e82d7-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e82d7-136">RELATED LINKS</span></span>

[<span data-ttu-id="e82d7-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e82d7-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="e82d7-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e82d7-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

