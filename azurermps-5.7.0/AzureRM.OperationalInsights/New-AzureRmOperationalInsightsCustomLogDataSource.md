---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: 510148c5d700c1378b0e468bbd5e8a9206491284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441289"
---
# <span data-ttu-id="a76b6-101">New-AzureRmOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="a76b6-101">New-AzureRmOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="a76b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a76b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a76b6-103">Define uma política de coleta de logs personalizada.</span><span class="sxs-lookup"><span data-stu-id="a76b6-103">Defines a custom log collection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a76b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a76b6-104">SYNTAX</span></span>

### <span data-ttu-id="a76b6-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a76b6-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a76b6-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a76b6-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a76b6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a76b6-107">DESCRIPTION</span></span>
<span data-ttu-id="a76b6-108">O cmdlet **New-AzureRmOperationalInsightsCustomLogDataSource** define uma política de coleta de log Personalizada.</span><span class="sxs-lookup"><span data-stu-id="a76b6-108">The **New-AzureRmOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="a76b6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a76b6-109">EXAMPLES</span></span>

## <span data-ttu-id="a76b6-110">OS</span><span class="sxs-lookup"><span data-stu-id="a76b6-110">PARAMETERS</span></span>

### <span data-ttu-id="a76b6-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="a76b6-111">-CustomLogRawJson</span></span>
<span data-ttu-id="a76b6-112">Especifica a política de coleção personalizada como uma cadeia de caracteres JSON (JavaScript Object Notation) bruta.</span><span class="sxs-lookup"><span data-stu-id="a76b6-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a76b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76b6-113">-DefaultProfile</span></span>
<span data-ttu-id="a76b6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a76b6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a76b6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a76b6-115">-Force</span></span>
<span data-ttu-id="a76b6-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a76b6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a76b6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a76b6-117">-Name</span></span>
<span data-ttu-id="a76b6-118">Especifica um nome para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="a76b6-118">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a76b6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a76b6-119">-ResourceGroupName</span></span>
<span data-ttu-id="a76b6-120">Especifica o nome de um grupo de recursos que contém computadores.</span><span class="sxs-lookup"><span data-stu-id="a76b6-120">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a76b6-121">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="a76b6-121">-Workspace</span></span>
<span data-ttu-id="a76b6-122">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="a76b6-122">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a76b6-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a76b6-123">-WorkspaceName</span></span>
<span data-ttu-id="a76b6-124">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="a76b6-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a76b6-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a76b6-125">-Confirm</span></span>
<span data-ttu-id="a76b6-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a76b6-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76b6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a76b6-127">-WhatIf</span></span>
<span data-ttu-id="a76b6-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a76b6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a76b6-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a76b6-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76b6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76b6-130">CommonParameters</span></span>
<span data-ttu-id="a76b6-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a76b6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76b6-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a76b6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76b6-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a76b6-133">INPUTS</span></span>

### <span data-ttu-id="a76b6-134">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a76b6-134">PSWorkspace</span></span>
<span data-ttu-id="a76b6-135">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a76b6-135">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="a76b6-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a76b6-136">OUTPUTS</span></span>

### <span data-ttu-id="a76b6-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a76b6-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a76b6-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a76b6-138">NOTES</span></span>

## <span data-ttu-id="a76b6-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a76b6-139">RELATED LINKS</span></span>

[<span data-ttu-id="a76b6-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="a76b6-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="a76b6-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="a76b6-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


