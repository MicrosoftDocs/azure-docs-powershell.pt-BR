---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
ms.openlocfilehash: c8ee3324f7f6e7653d86bef747bdb9831982474e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429085"
---
# <span data-ttu-id="57950-101">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="57950-101">Update-AzureRmServiceFabricReliability</span></span>

## <span data-ttu-id="57950-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57950-102">SYNOPSIS</span></span>
<span data-ttu-id="57950-103">Atualize a camada de confiabilidade do tipo de nó primário em um cluster.</span><span class="sxs-lookup"><span data-stu-id="57950-103">Update the reliability tier of the primary node type in a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57950-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57950-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57950-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57950-105">DESCRIPTION</span></span>
<span data-ttu-id="57950-106">Use **Update-AzureRmServiceFabricReliability** para atualizar a confiabilidade do tipo de nó primário em um cluster.</span><span class="sxs-lookup"><span data-stu-id="57950-106">Use **Update-AzureRmServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="57950-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57950-107">EXAMPLES</span></span>

### <span data-ttu-id="57950-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="57950-108">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="57950-109">Esse comando altera a camada de confiabilidade do tipo de nó principal para prata.</span><span class="sxs-lookup"><span data-stu-id="57950-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="57950-110">OS</span><span class="sxs-lookup"><span data-stu-id="57950-110">PARAMETERS</span></span>

### <span data-ttu-id="57950-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="57950-111">-AutoAddNode</span></span>
<span data-ttu-id="57950-112">Adicionar contagem de nós automaticamente ao alterar a confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="57950-112">Add node count automatically when changing reliability.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: Auto

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57950-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="57950-113">-Name</span></span>
<span data-ttu-id="57950-114">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="57950-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57950-115">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="57950-115">-ReliabilityLevel</span></span>
<span data-ttu-id="57950-116">Camada de confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="57950-116">Reliability tier.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, Bronze, Silver, Gold, Platinum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57950-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57950-117">-ResourceGroupName</span></span>
<span data-ttu-id="57950-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="57950-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="57950-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="57950-119">-Confirm</span></span>
<span data-ttu-id="57950-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57950-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57950-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57950-121">-WhatIf</span></span>
<span data-ttu-id="57950-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57950-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57950-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57950-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57950-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57950-124">-DefaultProfile</span></span>
<span data-ttu-id="57950-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57950-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57950-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57950-126">CommonParameters</span></span>
<span data-ttu-id="57950-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57950-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57950-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57950-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57950-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57950-129">INPUTS</span></span>

### <span data-ttu-id="57950-130">Microsoft. Azure. Commands. imfabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="57950-130">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>
<span data-ttu-id="57950-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="57950-131">System.Management.Automation.SwitchParameter</span></span>

<span data-ttu-id="57950-132">System. String</span><span class="sxs-lookup"><span data-stu-id="57950-132">System.String</span></span>

## <span data-ttu-id="57950-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57950-133">OUTPUTS</span></span>

### <span data-ttu-id="57950-134">Microsoft. Azure. Commands. imfabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="57950-134">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="57950-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57950-135">NOTES</span></span>

## <span data-ttu-id="57950-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57950-136">RELATED LINKS</span></span>

