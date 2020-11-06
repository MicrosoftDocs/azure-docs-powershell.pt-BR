---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 4b63568b4a2bfd6b79c51fcd906819f4831a7ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609549"
---
# <span data-ttu-id="42243-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="42243-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="42243-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42243-102">SYNOPSIS</span></span>
<span data-ttu-id="42243-103">Obtém um cofre de retenção de longo prazo do servidor.</span><span class="sxs-lookup"><span data-stu-id="42243-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42243-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42243-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42243-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42243-105">DESCRIPTION</span></span>
<span data-ttu-id="42243-106">O cmdlet **Get-AzureRmSqlServerBackupLongTermRetentionVault** Obtém o cofre de retenção de longo prazo registrado neste servidor.</span><span class="sxs-lookup"><span data-stu-id="42243-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="42243-107">O cofre é um recurso de backup do Azure usado para armazenar dados de backup.</span><span class="sxs-lookup"><span data-stu-id="42243-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="42243-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42243-108">EXAMPLES</span></span>

## <span data-ttu-id="42243-109">OS</span><span class="sxs-lookup"><span data-stu-id="42243-109">PARAMETERS</span></span>

### <span data-ttu-id="42243-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42243-110">-ResourceGroupName</span></span>
<span data-ttu-id="42243-111">Especifica o nome do grupo de recursos que contém o servidor.</span><span class="sxs-lookup"><span data-stu-id="42243-111">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="42243-112">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="42243-112">-ServerName</span></span>
<span data-ttu-id="42243-113">Especifica o servidor para o qual esse cmdlet obtém um cofre.</span><span class="sxs-lookup"><span data-stu-id="42243-113">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="42243-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="42243-114">-Confirm</span></span>
<span data-ttu-id="42243-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42243-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42243-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42243-116">-WhatIf</span></span>
<span data-ttu-id="42243-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="42243-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42243-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="42243-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42243-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42243-119">-DefaultProfile</span></span>
<span data-ttu-id="42243-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42243-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42243-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42243-121">CommonParameters</span></span>
<span data-ttu-id="42243-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42243-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42243-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42243-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42243-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42243-124">INPUTS</span></span>

## <span data-ttu-id="42243-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42243-125">OUTPUTS</span></span>

## <span data-ttu-id="42243-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42243-126">NOTES</span></span>

## <span data-ttu-id="42243-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42243-127">RELATED LINKS</span></span>

[<span data-ttu-id="42243-128">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="42243-128">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="42243-129">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="42243-129">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

