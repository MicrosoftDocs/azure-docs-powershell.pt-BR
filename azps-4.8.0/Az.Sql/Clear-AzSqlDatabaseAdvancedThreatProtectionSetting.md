---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 7bdfb6ef415cdf5f3cac173730770307701b50bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954665"
---
# <span data-ttu-id="28ab3-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="28ab3-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="28ab3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="28ab3-103">Remove as configurações avançadas de proteção contra ameaças de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="28ab3-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="28ab3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28ab3-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28ab3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="28ab3-106">O cmdlet **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** remove as configurações avançadas de proteção contra ameaças de um banco de dados SQL do AzureAzure.</span><span class="sxs-lookup"><span data-stu-id="28ab3-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="28ab3-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* e *nomedoservidor* para identificar o banco de dados do qual esse cmdlet Remove as configurações.</span><span class="sxs-lookup"><span data-stu-id="28ab3-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="28ab3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28ab3-108">EXAMPLES</span></span>

### <span data-ttu-id="28ab3-109">Exemplo 1: remover as configurações avançadas de proteção contra ameaças de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="28ab3-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="28ab3-110">Esse comando remove as configurações avançadas de proteção contra ameaças de um banco de dados denominado Database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="28ab3-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="28ab3-111">OS</span><span class="sxs-lookup"><span data-stu-id="28ab3-111">PARAMETERS</span></span>

### <span data-ttu-id="28ab3-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="28ab3-112">-DatabaseName</span></span>
<span data-ttu-id="28ab3-113">Especifica o nome de um banco de dados onde as configurações avançadas de proteção contra ameaças devem ser removidas.</span><span class="sxs-lookup"><span data-stu-id="28ab3-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="28ab3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ab3-114">-DefaultProfile</span></span>
<span data-ttu-id="28ab3-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="28ab3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28ab3-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28ab3-116">-PassThru</span></span>
<span data-ttu-id="28ab3-117">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="28ab3-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="28ab3-118">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="28ab3-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ab3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28ab3-119">-ResourceGroupName</span></span>
<span data-ttu-id="28ab3-120">Especifica o nome do grupo de recursos que o servidor pertence.</span><span class="sxs-lookup"><span data-stu-id="28ab3-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="28ab3-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="28ab3-121">-ServerName</span></span>
<span data-ttu-id="28ab3-122">Especifica o nome de um servidor no qual o banco de dados é executado.</span><span class="sxs-lookup"><span data-stu-id="28ab3-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="28ab3-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="28ab3-123">-Confirm</span></span>
<span data-ttu-id="28ab3-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28ab3-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ab3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28ab3-125">-WhatIf</span></span>
<span data-ttu-id="28ab3-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28ab3-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28ab3-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28ab3-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ab3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ab3-128">CommonParameters</span></span>
<span data-ttu-id="28ab3-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28ab3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ab3-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28ab3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ab3-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28ab3-131">INPUTS</span></span>

### <span data-ttu-id="28ab3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="28ab3-132">System.String</span></span>

## <span data-ttu-id="28ab3-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28ab3-133">OUTPUTS</span></span>

### <span data-ttu-id="28ab3-134">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="28ab3-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="28ab3-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28ab3-135">NOTES</span></span>

## <span data-ttu-id="28ab3-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28ab3-136">RELATED LINKS</span></span>

[<span data-ttu-id="28ab3-137">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="28ab3-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


