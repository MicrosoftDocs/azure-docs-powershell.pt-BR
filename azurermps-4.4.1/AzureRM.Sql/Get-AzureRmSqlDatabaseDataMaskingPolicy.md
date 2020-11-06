---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 13ab762b7f5ed8457bc8975687c3a45315be969b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610704"
---
# <span data-ttu-id="fca54-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="fca54-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="fca54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fca54-102">SYNOPSIS</span></span>
<span data-ttu-id="fca54-103">Obtém a política de máscara de dados de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fca54-103">Gets the data masking policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fca54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fca54-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fca54-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fca54-105">DESCRIPTION</span></span>
<span data-ttu-id="fca54-106">O cmdlet **Get-AzureRmSqlDatabaseDataMaskingPolicy** Obtém a política de máscara de dados de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fca54-106">The **Get-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="fca54-107">Para usar esse cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fca54-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="fca54-108">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="fca54-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="fca54-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fca54-109">EXAMPLES</span></span>

### <span data-ttu-id="fca54-110">Exemplo 1: obter a política de máscara de dados de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="fca54-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="fca54-111">Esse comando obtém a política de máscara de dados do banco de dados Database01 no grupo ResourceGroup01 de recursos no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="fca54-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="fca54-112">OS</span><span class="sxs-lookup"><span data-stu-id="fca54-112">PARAMETERS</span></span>

### <span data-ttu-id="fca54-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fca54-113">-DatabaseName</span></span>
<span data-ttu-id="fca54-114">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fca54-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="fca54-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca54-115">-ResourceGroupName</span></span>
<span data-ttu-id="fca54-116">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="fca54-116">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="fca54-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="fca54-117">-ServerName</span></span>
<span data-ttu-id="fca54-118">Especifica o nome do servidor no qual o banco de dados está localizado.</span><span class="sxs-lookup"><span data-stu-id="fca54-118">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="fca54-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fca54-119">-Confirm</span></span>
<span data-ttu-id="fca54-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fca54-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fca54-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fca54-121">-WhatIf</span></span>
<span data-ttu-id="fca54-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fca54-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fca54-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fca54-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fca54-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fca54-124">-DefaultProfile</span></span>
<span data-ttu-id="fca54-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fca54-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fca54-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca54-126">CommonParameters</span></span>
<span data-ttu-id="fca54-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fca54-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca54-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fca54-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca54-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fca54-129">INPUTS</span></span>

## <span data-ttu-id="fca54-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fca54-130">OUTPUTS</span></span>

### <span data-ttu-id="fca54-131">Microsoft. Azure. Commands. Sql. Security. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fca54-131">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="fca54-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fca54-132">NOTES</span></span>

## <span data-ttu-id="fca54-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fca54-133">RELATED LINKS</span></span>

[<span data-ttu-id="fca54-134">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fca54-134">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fca54-135">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fca54-135">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fca54-136">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fca54-136">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fca54-137">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="fca54-137">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="fca54-138">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fca54-138">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


