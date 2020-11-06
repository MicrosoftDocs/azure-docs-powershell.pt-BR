---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1C0AF5B2-7187-4BFA-8DBB-A771FD2E00A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a4538210c95f8357a9b920f827e8812b47377a2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429054"
---
# <span data-ttu-id="df133-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="df133-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="df133-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df133-102">SYNOPSIS</span></span>
<span data-ttu-id="df133-103">Obtém uma política de retenção de longo prazo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="df133-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df133-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df133-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df133-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df133-105">DESCRIPTION</span></span>
<span data-ttu-id="df133-106">O cmdlet **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** Obtém a política de retenção de longo prazo registrada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="df133-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="df133-107">A política é um recurso de backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="df133-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="df133-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df133-108">EXAMPLES</span></span>

## <span data-ttu-id="df133-109">OS</span><span class="sxs-lookup"><span data-stu-id="df133-109">PARAMETERS</span></span>

### <span data-ttu-id="df133-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="df133-110">-DatabaseName</span></span>
<span data-ttu-id="df133-111">Especifica o nome do banco de dados SQL para o qual esse cmdlet obtém uma política.</span><span class="sxs-lookup"><span data-stu-id="df133-111">Specifies the name of the SQL Database for which this cmdlet gets a policy.</span></span>

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

### <span data-ttu-id="df133-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df133-112">-ResourceGroupName</span></span>
<span data-ttu-id="df133-113">Especifica o nome do grupo de recursos que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="df133-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="df133-114">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="df133-114">-ServerName</span></span>
<span data-ttu-id="df133-115">Especifica o servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="df133-115">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="df133-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="df133-116">-Confirm</span></span>
<span data-ttu-id="df133-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df133-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df133-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df133-118">-WhatIf</span></span>
<span data-ttu-id="df133-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df133-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df133-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df133-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df133-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df133-121">-DefaultProfile</span></span>
<span data-ttu-id="df133-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df133-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df133-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df133-123">CommonParameters</span></span>
<span data-ttu-id="df133-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df133-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df133-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df133-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df133-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df133-126">INPUTS</span></span>

## <span data-ttu-id="df133-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df133-127">OUTPUTS</span></span>

## <span data-ttu-id="df133-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df133-128">NOTES</span></span>

## <span data-ttu-id="df133-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df133-129">RELATED LINKS</span></span>

[<span data-ttu-id="df133-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="df133-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="df133-131">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="df133-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
