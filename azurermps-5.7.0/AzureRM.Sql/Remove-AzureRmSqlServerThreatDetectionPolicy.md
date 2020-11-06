---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: d9763bf02054962eac955188860e97ed271d7a7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428726"
---
# <span data-ttu-id="bec54-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bec54-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="bec54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bec54-102">SYNOPSIS</span></span>
<span data-ttu-id="bec54-103">Remove a política de detecção de ameaças de um servidor.</span><span class="sxs-lookup"><span data-stu-id="bec54-103">Removes the threat detection policy from a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bec54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bec54-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bec54-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bec54-105">DESCRIPTION</span></span>
<span data-ttu-id="bec54-106">O cmdlet Remove-AzureRmSqlServerThreatDetectionPolicy remove a política de detecção de ameaças de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="bec54-106">The Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>

<span data-ttu-id="bec54-107">Para usar esse cmdlet, especifique os parâmetros ResourceGroupName e nomedoservidor para identificar o servidor do qual esse cmdlet Remove a política.</span><span class="sxs-lookup"><span data-stu-id="bec54-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="bec54-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bec54-108">EXAMPLES</span></span>

### <span data-ttu-id="bec54-109">Exemplo 1: remover uma política de detecção de ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="bec54-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\> Remove-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="bec54-110">Esse comando Remove a política de detecção de ameaças de um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="bec54-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="bec54-111">OS</span><span class="sxs-lookup"><span data-stu-id="bec54-111">PARAMETERS</span></span>

### <span data-ttu-id="bec54-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec54-112">-DefaultProfile</span></span>
<span data-ttu-id="bec54-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bec54-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec54-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bec54-114">-PassThru</span></span>
<span data-ttu-id="bec54-115">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="bec54-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bec54-116">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="bec54-116">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec54-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec54-117">-ResourceGroupName</span></span>
<span data-ttu-id="bec54-118">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="bec54-118">Specifies the name of the resource group the server is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec54-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="bec54-119">-ServerName</span></span>
<span data-ttu-id="bec54-120">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="bec54-120">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec54-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bec54-121">-Confirm</span></span>
<span data-ttu-id="bec54-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bec54-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec54-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec54-123">-WhatIf</span></span>
<span data-ttu-id="bec54-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bec54-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bec54-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bec54-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec54-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec54-126">CommonParameters</span></span>
<span data-ttu-id="bec54-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec54-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec54-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec54-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec54-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bec54-129">INPUTS</span></span>

###  
<span data-ttu-id="bec54-130">Não é possível canalizar a entrada para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bec54-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="bec54-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bec54-131">OUTPUTS</span></span>

### <span data-ttu-id="bec54-132">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="bec54-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="bec54-133">Esse cmdlet retorna um objeto ServerThreatDetectionPolicyModel.</span><span class="sxs-lookup"><span data-stu-id="bec54-133">This cmdlet returns a ServerThreatDetectionPolicyModel object.</span></span>

## <span data-ttu-id="bec54-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bec54-134">NOTES</span></span>

## <span data-ttu-id="bec54-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bec54-135">RELATED LINKS</span></span>

[<span data-ttu-id="bec54-136">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="bec54-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

