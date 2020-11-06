---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: e6a47578ef2442e6ca2f6d03284624f1f2906e35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428238"
---
# <span data-ttu-id="618c1-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="618c1-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="618c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="618c1-102">SYNOPSIS</span></span>
<span data-ttu-id="618c1-103">Remove a política de detecção de ameaças de um servidor.</span><span class="sxs-lookup"><span data-stu-id="618c1-103">Removes the threat detection policy from a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="618c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="618c1-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="618c1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="618c1-105">DESCRIPTION</span></span>
<span data-ttu-id="618c1-106">O cmdlet Remove-AzureRmSqlServerThreatDetectionPolicy remove a política de detecção de ameaças de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="618c1-106">The Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>

<span data-ttu-id="618c1-107">Para usar esse cmdlet, especifique os parâmetros ResourceGroupName e nomedoservidor para identificar o servidor do qual esse cmdlet Remove a política.</span><span class="sxs-lookup"><span data-stu-id="618c1-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="618c1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="618c1-108">EXAMPLES</span></span>

### <span data-ttu-id="618c1-109">--------------------------Exemplo 1: remover uma política de detecção de ameaças para um banco de dados--------------------------</span><span class="sxs-lookup"><span data-stu-id="618c1-109">--------------------------  Example 1: Remove a threat detection policy for a database  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="618c1-110">Esse comando Remove a política de detecção de ameaças de um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="618c1-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="618c1-111">OS</span><span class="sxs-lookup"><span data-stu-id="618c1-111">PARAMETERS</span></span>

### <span data-ttu-id="618c1-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="618c1-112">-PassThru</span></span>
<span data-ttu-id="618c1-113">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="618c1-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="618c1-114">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="618c1-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="618c1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="618c1-115">-ResourceGroupName</span></span>
<span data-ttu-id="618c1-116">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="618c1-116">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="618c1-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="618c1-117">-ServerName</span></span>
<span data-ttu-id="618c1-118">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="618c1-118">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="618c1-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="618c1-119">-Confirm</span></span>
<span data-ttu-id="618c1-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="618c1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="618c1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="618c1-121">-WhatIf</span></span>
<span data-ttu-id="618c1-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="618c1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="618c1-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="618c1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="618c1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="618c1-124">-DefaultProfile</span></span>
<span data-ttu-id="618c1-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="618c1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="618c1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="618c1-126">CommonParameters</span></span>
<span data-ttu-id="618c1-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="618c1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="618c1-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="618c1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="618c1-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="618c1-129">INPUTS</span></span>

###  
<span data-ttu-id="618c1-130">Não é possível canalizar a entrada para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="618c1-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="618c1-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="618c1-131">OUTPUTS</span></span>

### <span data-ttu-id="618c1-132">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="618c1-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="618c1-133">Esse cmdlet retorna um objeto ServerThreatDetectionPolicyModel.</span><span class="sxs-lookup"><span data-stu-id="618c1-133">This cmdlet returns a ServerThreatDetectionPolicyModel object.</span></span>

## <span data-ttu-id="618c1-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="618c1-134">NOTES</span></span>

## <span data-ttu-id="618c1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="618c1-135">RELATED LINKS</span></span>

[<span data-ttu-id="618c1-136">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="618c1-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

