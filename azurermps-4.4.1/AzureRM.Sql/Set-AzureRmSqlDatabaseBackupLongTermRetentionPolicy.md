---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 196E1AC9-A1E2-47D2-A3C1-535EFE439EE8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 1bfe5d721930288c65a18be8ccba2ebfe2f90484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430604"
---
# <span data-ttu-id="2796c-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2796c-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="2796c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2796c-102">SYNOPSIS</span></span>
<span data-ttu-id="2796c-103">Define uma política de retenção de longo prazo do servidor.</span><span class="sxs-lookup"><span data-stu-id="2796c-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2796c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2796c-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2796c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2796c-105">DESCRIPTION</span></span>
<span data-ttu-id="2796c-106">O cmdlet **set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** define a política de retenção de longo prazo registrada para esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2796c-106">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="2796c-107">A política é um recurso de backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="2796c-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="2796c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2796c-108">EXAMPLES</span></span>

## <span data-ttu-id="2796c-109">OS</span><span class="sxs-lookup"><span data-stu-id="2796c-109">PARAMETERS</span></span>

### <span data-ttu-id="2796c-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2796c-110">-DatabaseName</span></span>
<span data-ttu-id="2796c-111">Especifica o nome do banco de dados SQL para o qual esse cmdlet define uma política.</span><span class="sxs-lookup"><span data-stu-id="2796c-111">Specifies the name of the SQL Database for which this cmdlet sets a policy.</span></span>

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

### <span data-ttu-id="2796c-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2796c-112">-ResourceGroupName</span></span>
<span data-ttu-id="2796c-113">Especifica o nome do grupo de recursos que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2796c-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="2796c-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2796c-114">-ResourceId</span></span>
<span data-ttu-id="2796c-115">Especifica a ID de um recurso.</span><span class="sxs-lookup"><span data-stu-id="2796c-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2796c-116">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2796c-116">-ServerName</span></span>
<span data-ttu-id="2796c-117">Especifica o servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2796c-117">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="2796c-118">-Estado</span><span class="sxs-lookup"><span data-stu-id="2796c-118">-State</span></span>
<span data-ttu-id="2796c-119">Especifica um estado.</span><span class="sxs-lookup"><span data-stu-id="2796c-119">Specifies a state.</span></span>

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

### <span data-ttu-id="2796c-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2796c-120">-Confirm</span></span>
<span data-ttu-id="2796c-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2796c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2796c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2796c-122">-WhatIf</span></span>
<span data-ttu-id="2796c-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2796c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2796c-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2796c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2796c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2796c-125">-DefaultProfile</span></span>
<span data-ttu-id="2796c-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2796c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2796c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2796c-127">CommonParameters</span></span>
<span data-ttu-id="2796c-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2796c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2796c-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2796c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2796c-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2796c-130">INPUTS</span></span>

## <span data-ttu-id="2796c-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2796c-131">OUTPUTS</span></span>

## <span data-ttu-id="2796c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2796c-132">NOTES</span></span>

## <span data-ttu-id="2796c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2796c-133">RELATED LINKS</span></span>

[<span data-ttu-id="2796c-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2796c-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="2796c-135">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="2796c-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
