---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: f574e8e67f249ac1c7a4a3878ecc93a0a1eabc5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428702"
---
# <span data-ttu-id="af4b5-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="af4b5-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="af4b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af4b5-102">SYNOPSIS</span></span>
<span data-ttu-id="af4b5-103">Define uma política de backup geográfico do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="af4b5-103">Sets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af4b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af4b5-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af4b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af4b5-105">DESCRIPTION</span></span>
<span data-ttu-id="af4b5-106">O cmdlet **set-AzureRmSqlDatabaseGeoBackupPolicy** define a política de backup geográfico registrada em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="af4b5-106">The **Set-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="af4b5-107">Este é um recurso de backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="af4b5-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="af4b5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af4b5-108">EXAMPLES</span></span>

## <span data-ttu-id="af4b5-109">OS</span><span class="sxs-lookup"><span data-stu-id="af4b5-109">PARAMETERS</span></span>

### <span data-ttu-id="af4b5-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="af4b5-110">-DatabaseName</span></span>
<span data-ttu-id="af4b5-111">Especifica o nome do banco de dados para o qual esse cmdlet define a política de backup geográfico.</span><span class="sxs-lookup"><span data-stu-id="af4b5-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="af4b5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af4b5-112">-DefaultProfile</span></span>
<span data-ttu-id="af4b5-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="af4b5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af4b5-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af4b5-114">-ResourceGroupName</span></span>
<span data-ttu-id="af4b5-115">Especifica o nome do grupo de recursos do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="af4b5-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="af4b5-116">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="af4b5-116">-ServerName</span></span>
<span data-ttu-id="af4b5-117">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="af4b5-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="af4b5-118">-Estado</span><span class="sxs-lookup"><span data-stu-id="af4b5-118">-State</span></span>
<span data-ttu-id="af4b5-119">Especifica o estado da política de backup geográfico.</span><span class="sxs-lookup"><span data-stu-id="af4b5-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="af4b5-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="af4b5-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="af4b5-121">Possibilita</span><span class="sxs-lookup"><span data-stu-id="af4b5-121">Enabled</span></span> 
- <span data-ttu-id="af4b5-122">Ativo</span><span class="sxs-lookup"><span data-stu-id="af4b5-122">Disabled</span></span>

```yaml
Type: GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4b5-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af4b5-123">-Confirm</span></span>
<span data-ttu-id="af4b5-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af4b5-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4b5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af4b5-125">-WhatIf</span></span>
<span data-ttu-id="af4b5-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af4b5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af4b5-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af4b5-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4b5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af4b5-128">CommonParameters</span></span>
<span data-ttu-id="af4b5-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af4b5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af4b5-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af4b5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af4b5-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af4b5-131">INPUTS</span></span>

### <span data-ttu-id="af4b5-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="af4b5-132">None</span></span>
<span data-ttu-id="af4b5-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="af4b5-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af4b5-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af4b5-134">OUTPUTS</span></span>

## <span data-ttu-id="af4b5-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af4b5-135">NOTES</span></span>

## <span data-ttu-id="af4b5-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af4b5-136">RELATED LINKS</span></span>

[<span data-ttu-id="af4b5-137">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="af4b5-137">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="af4b5-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="af4b5-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

