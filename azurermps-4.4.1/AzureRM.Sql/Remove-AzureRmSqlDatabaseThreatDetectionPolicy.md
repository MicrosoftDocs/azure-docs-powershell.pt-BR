---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 723e765435aae739e6d58320276f7df8ac06ba66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441375"
---
# <span data-ttu-id="2a2a9-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2a2a9-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="2a2a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a2a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2a2a9-103">Remove a política de detecção de ameaças de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-103">Removes the threat detection policy from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a2a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a2a9-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a2a9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a2a9-105">DESCRIPTION</span></span>
<span data-ttu-id="2a2a9-106">O cmdlet **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** remove a política de detecção de ameaças de um banco de dados SQL do AzureAzure.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-106">The **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="2a2a9-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* e *nomedoservidor* para identificar o banco de dados do qual esse cmdlet Remove a política.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="2a2a9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a2a9-108">EXAMPLES</span></span>

### <span data-ttu-id="2a2a9-109">Exemplo 1: remover uma política de detecção de ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="2a2a9-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="2a2a9-110">Esse comando Remove a política de detecção de ameaças de um banco de dados chamado Database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="2a2a9-111">OS</span><span class="sxs-lookup"><span data-stu-id="2a2a9-111">PARAMETERS</span></span>

### <span data-ttu-id="2a2a9-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2a2a9-112">-DatabaseName</span></span>
<span data-ttu-id="2a2a9-113">Especifica o nome de um banco de dados no qual a política de detecção de ameaças deve ser removida.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

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

### <span data-ttu-id="2a2a9-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a2a9-114">-PassThru</span></span>
<span data-ttu-id="2a2a9-115">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2a2a9-116">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2a2a9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a2a9-117">-ResourceGroupName</span></span>
<span data-ttu-id="2a2a9-118">Especifica o nome do grupo de recursos que o servidor pertence.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-118">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="2a2a9-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2a2a9-119">-ServerName</span></span>
<span data-ttu-id="2a2a9-120">Especifica o nome de um servidor no qual o banco de dados é executado.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-120">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="2a2a9-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2a2a9-121">-Confirm</span></span>
<span data-ttu-id="2a2a9-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a2a9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a2a9-123">-WhatIf</span></span>
<span data-ttu-id="2a2a9-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a2a9-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a2a9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a2a9-126">-DefaultProfile</span></span>
<span data-ttu-id="2a2a9-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a2a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a2a9-128">CommonParameters</span></span>
<span data-ttu-id="2a2a9-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a2a9-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a2a9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a2a9-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a2a9-131">INPUTS</span></span>

###  
<span data-ttu-id="2a2a9-132">Não é possível canalizar a entrada para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a2a9-132">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="2a2a9-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a2a9-133">OUTPUTS</span></span>

### <span data-ttu-id="2a2a9-134">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2a2a9-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="2a2a9-135">Esse cmdlet retorna um objeto **DatabaseThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="2a2a9-135">This cmdlet returns a **DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="2a2a9-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a2a9-136">NOTES</span></span>

## <span data-ttu-id="2a2a9-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a2a9-137">RELATED LINKS</span></span>

[<span data-ttu-id="2a2a9-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="2a2a9-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


