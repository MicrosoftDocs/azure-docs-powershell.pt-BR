---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7642F18A-B193-4849-BE3C-1B85FBD213F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: e76ba16f9578eefdce36a1f3d726e027be2a9ed6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440713"
---
# <span data-ttu-id="940ee-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="940ee-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="940ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="940ee-102">SYNOPSIS</span></span>
<span data-ttu-id="940ee-103">Define um cofre de retenção de longo prazo do servidor.</span><span class="sxs-lookup"><span data-stu-id="940ee-103">Sets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="940ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="940ee-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerBackupLongTermRetentionVault -ResourceId <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="940ee-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="940ee-105">DESCRIPTION</span></span>
<span data-ttu-id="940ee-106">O cmdlet **set-AzureRmSqlServerBackupLongTermRetentionVault** define o cofre de retenção de longo prazo registrado para este servidor.</span><span class="sxs-lookup"><span data-stu-id="940ee-106">The **Set-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet sets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="940ee-107">O cofre é um recurso de backup do Azure usado para armazenar dados de backup.</span><span class="sxs-lookup"><span data-stu-id="940ee-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="940ee-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="940ee-108">EXAMPLES</span></span>

## <span data-ttu-id="940ee-109">OS</span><span class="sxs-lookup"><span data-stu-id="940ee-109">PARAMETERS</span></span>

### <span data-ttu-id="940ee-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="940ee-110">-DefaultProfile</span></span>
<span data-ttu-id="940ee-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="940ee-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="940ee-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="940ee-112">-ResourceGroupName</span></span>
<span data-ttu-id="940ee-113">Especifica o nome do grupo de recursos que contém o servidor.</span><span class="sxs-lookup"><span data-stu-id="940ee-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="940ee-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="940ee-114">-ResourceId</span></span>
<span data-ttu-id="940ee-115">Especifica a ID de um recurso.</span><span class="sxs-lookup"><span data-stu-id="940ee-115">Specifies the ID of a resource.</span></span>

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

### <span data-ttu-id="940ee-116">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="940ee-116">-ServerName</span></span>
<span data-ttu-id="940ee-117">Especifica o servidor para o qual esse cmdlet define um cofre.</span><span class="sxs-lookup"><span data-stu-id="940ee-117">Specifies the server for which this cmdlet sets a vault.</span></span>

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

### <span data-ttu-id="940ee-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="940ee-118">-Confirm</span></span>
<span data-ttu-id="940ee-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="940ee-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="940ee-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="940ee-120">-WhatIf</span></span>
<span data-ttu-id="940ee-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="940ee-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="940ee-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="940ee-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="940ee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="940ee-123">CommonParameters</span></span>
<span data-ttu-id="940ee-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="940ee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="940ee-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="940ee-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="940ee-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="940ee-126">INPUTS</span></span>

### <span data-ttu-id="940ee-127">System. String</span><span class="sxs-lookup"><span data-stu-id="940ee-127">System.String</span></span>

## <span data-ttu-id="940ee-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="940ee-128">OUTPUTS</span></span>

### <span data-ttu-id="940ee-129">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlServerBackupLongTermRetentionVaultModel</span><span class="sxs-lookup"><span data-stu-id="940ee-129">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlServerBackupLongTermRetentionVaultModel</span></span>

## <span data-ttu-id="940ee-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="940ee-130">NOTES</span></span>

## <span data-ttu-id="940ee-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="940ee-131">RELATED LINKS</span></span>

[<span data-ttu-id="940ee-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="940ee-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Get-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="940ee-133">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="940ee-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)