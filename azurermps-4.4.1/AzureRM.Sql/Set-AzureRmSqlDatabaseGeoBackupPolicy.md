---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 2cf85aac2d301653787bdf227db1cd187a887986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429036"
---
# <span data-ttu-id="54e92-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="54e92-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="54e92-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54e92-102">SYNOPSIS</span></span>
<span data-ttu-id="54e92-103">Define uma política de backup geográfico do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="54e92-103">Sets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54e92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54e92-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54e92-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54e92-105">DESCRIPTION</span></span>
<span data-ttu-id="54e92-106">O cmdlet **set-AzureRmSqlDatabaseGeoBackupPolicy** define a política de backup geográfico registrada em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="54e92-106">The **Set-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="54e92-107">Este é um recurso de backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="54e92-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="54e92-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54e92-108">EXAMPLES</span></span>

## <span data-ttu-id="54e92-109">OS</span><span class="sxs-lookup"><span data-stu-id="54e92-109">PARAMETERS</span></span>

### <span data-ttu-id="54e92-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="54e92-110">-DatabaseName</span></span>
<span data-ttu-id="54e92-111">Especifica o nome do banco de dados para o qual esse cmdlet define a política de backup geográfico.</span><span class="sxs-lookup"><span data-stu-id="54e92-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="54e92-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54e92-112">-ResourceGroupName</span></span>
<span data-ttu-id="54e92-113">Especifica o nome do grupo de recursos do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="54e92-113">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="54e92-114">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="54e92-114">-ServerName</span></span>
<span data-ttu-id="54e92-115">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="54e92-115">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="54e92-116">-Estado</span><span class="sxs-lookup"><span data-stu-id="54e92-116">-State</span></span>
<span data-ttu-id="54e92-117">Especifica o estado da política de backup geográfico.</span><span class="sxs-lookup"><span data-stu-id="54e92-117">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="54e92-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="54e92-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="54e92-119">Possibilita</span><span class="sxs-lookup"><span data-stu-id="54e92-119">Enabled</span></span> 
- <span data-ttu-id="54e92-120">Ativo</span><span class="sxs-lookup"><span data-stu-id="54e92-120">Disabled</span></span>

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

### <span data-ttu-id="54e92-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="54e92-121">-Confirm</span></span>
<span data-ttu-id="54e92-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54e92-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54e92-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54e92-123">-WhatIf</span></span>
<span data-ttu-id="54e92-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="54e92-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54e92-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="54e92-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54e92-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e92-126">-DefaultProfile</span></span>
<span data-ttu-id="54e92-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="54e92-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54e92-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e92-128">CommonParameters</span></span>
<span data-ttu-id="54e92-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54e92-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e92-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54e92-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e92-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54e92-131">INPUTS</span></span>

## <span data-ttu-id="54e92-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54e92-132">OUTPUTS</span></span>

## <span data-ttu-id="54e92-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54e92-133">NOTES</span></span>

## <span data-ttu-id="54e92-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54e92-134">RELATED LINKS</span></span>

[<span data-ttu-id="54e92-135">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="54e92-135">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="54e92-136">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="54e92-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

