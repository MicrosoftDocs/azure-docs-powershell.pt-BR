---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5b75c2058fb7a6ddf323ebeaa6aad6967dcb5b01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598824"
---
# <span data-ttu-id="32b8b-101">Remove-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="32b8b-101">Remove-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="32b8b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="32b8b-103">Remove a política de detecção de ameaças de um servidor.</span><span class="sxs-lookup"><span data-stu-id="32b8b-103">Removes the threat detection policy from a server.</span></span>

## <span data-ttu-id="32b8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32b8b-104">SYNTAX</span></span>

```
Remove-AzSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32b8b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32b8b-105">DESCRIPTION</span></span>
<span data-ttu-id="32b8b-106">O cmdlet Remove-AzSqlServerThreatDetectionPolicy remove a política de detecção de ameaças de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="32b8b-106">The Remove-AzSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>
<span data-ttu-id="32b8b-107">Para usar esse cmdlet, especifique os parâmetros ResourceGroupName e nomedoservidor para identificar o servidor do qual esse cmdlet Remove a política.</span><span class="sxs-lookup"><span data-stu-id="32b8b-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="32b8b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32b8b-108">EXAMPLES</span></span>

### <span data-ttu-id="32b8b-109">Exemplo 1: remover uma política de detecção de ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="32b8b-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\> Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="32b8b-110">Esse comando Remove a política de detecção de ameaças de um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="32b8b-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="32b8b-111">OS</span><span class="sxs-lookup"><span data-stu-id="32b8b-111">PARAMETERS</span></span>

### <span data-ttu-id="32b8b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b8b-112">-DefaultProfile</span></span>
<span data-ttu-id="32b8b-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="32b8b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32b8b-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32b8b-114">-PassThru</span></span>
<span data-ttu-id="32b8b-115">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="32b8b-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="32b8b-116">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="32b8b-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="32b8b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32b8b-117">-ResourceGroupName</span></span>
<span data-ttu-id="32b8b-118">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="32b8b-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="32b8b-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="32b8b-119">-ServerName</span></span>
<span data-ttu-id="32b8b-120">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="32b8b-120">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32b8b-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="32b8b-121">-Confirm</span></span>
<span data-ttu-id="32b8b-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32b8b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32b8b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b8b-123">-WhatIf</span></span>
<span data-ttu-id="32b8b-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32b8b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32b8b-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32b8b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32b8b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b8b-126">CommonParameters</span></span>
<span data-ttu-id="32b8b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32b8b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b8b-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32b8b-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b8b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32b8b-129">INPUTS</span></span>

### <span data-ttu-id="32b8b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="32b8b-130">System.String</span></span>

## <span data-ttu-id="32b8b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32b8b-131">OUTPUTS</span></span>

### <span data-ttu-id="32b8b-132">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="32b8b-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="32b8b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32b8b-133">NOTES</span></span>

## <span data-ttu-id="32b8b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32b8b-134">RELATED LINKS</span></span>

[<span data-ttu-id="32b8b-135">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="32b8b-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

