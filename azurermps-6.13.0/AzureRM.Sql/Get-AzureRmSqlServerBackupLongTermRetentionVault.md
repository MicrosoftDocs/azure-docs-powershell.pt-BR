---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 0aeee8e991d0f74a341a750e69016b12027fe584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430829"
---
# <span data-ttu-id="2bd51-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="2bd51-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="2bd51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bd51-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd51-103">Obtém um cofre de retenção de longo prazo do servidor.</span><span class="sxs-lookup"><span data-stu-id="2bd51-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bd51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bd51-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bd51-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bd51-105">DESCRIPTION</span></span>
<span data-ttu-id="2bd51-106">O cmdlet **Get-AzureRmSqlServerBackupLongTermRetentionVault** Obtém o cofre de retenção de longo prazo registrado neste servidor.</span><span class="sxs-lookup"><span data-stu-id="2bd51-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="2bd51-107">O cofre é um recurso de backup do Azure usado para armazenar dados de backup.</span><span class="sxs-lookup"><span data-stu-id="2bd51-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="2bd51-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bd51-108">EXAMPLES</span></span>

## <span data-ttu-id="2bd51-109">OS</span><span class="sxs-lookup"><span data-stu-id="2bd51-109">PARAMETERS</span></span>

### <span data-ttu-id="2bd51-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd51-110">-DefaultProfile</span></span>
<span data-ttu-id="2bd51-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2bd51-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2bd51-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd51-112">-ResourceGroupName</span></span>
<span data-ttu-id="2bd51-113">Especifica o nome do grupo de recursos que contém o servidor.</span><span class="sxs-lookup"><span data-stu-id="2bd51-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="2bd51-114">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2bd51-114">-ServerName</span></span>
<span data-ttu-id="2bd51-115">Especifica o servidor para o qual esse cmdlet obtém um cofre.</span><span class="sxs-lookup"><span data-stu-id="2bd51-115">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="2bd51-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2bd51-116">-Confirm</span></span>
<span data-ttu-id="2bd51-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd51-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd51-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd51-118">-WhatIf</span></span>
<span data-ttu-id="2bd51-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2bd51-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bd51-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2bd51-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bd51-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd51-121">CommonParameters</span></span>
<span data-ttu-id="2bd51-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd51-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd51-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bd51-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd51-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bd51-124">INPUTS</span></span>

### <span data-ttu-id="2bd51-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2bd51-125">System.String</span></span>

## <span data-ttu-id="2bd51-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bd51-126">OUTPUTS</span></span>

### <span data-ttu-id="2bd51-127">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlServerBackupLongTermRetentionVaultModel</span><span class="sxs-lookup"><span data-stu-id="2bd51-127">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlServerBackupLongTermRetentionVaultModel</span></span>

## <span data-ttu-id="2bd51-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bd51-128">NOTES</span></span>

## <span data-ttu-id="2bd51-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bd51-129">RELATED LINKS</span></span>

[<span data-ttu-id="2bd51-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="2bd51-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="2bd51-131">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="2bd51-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

