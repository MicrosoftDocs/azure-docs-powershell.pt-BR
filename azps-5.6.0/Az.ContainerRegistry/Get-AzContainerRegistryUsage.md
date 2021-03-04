---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 7a950bc3b375ea9d86ef71eda120ac1d92fbd8e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890286"
---
# <span data-ttu-id="ea459-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="ea459-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="ea459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea459-102">SYNOPSIS</span></span>
<span data-ttu-id="ea459-103">Obter o uso de um registro de contêiner do azure.</span><span class="sxs-lookup"><span data-stu-id="ea459-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ea459-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ea459-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea459-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ea459-105">DESCRIPTION</span></span>
<span data-ttu-id="ea459-106">Obter o uso de um registro de contêiner do azure.</span><span class="sxs-lookup"><span data-stu-id="ea459-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ea459-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea459-107">EXAMPLES</span></span>

### <span data-ttu-id="ea459-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea459-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="ea459-109">Obter o uso de um registro de contêiner do azure.</span><span class="sxs-lookup"><span data-stu-id="ea459-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ea459-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ea459-110">PARAMETERS</span></span>

### <span data-ttu-id="ea459-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea459-111">-DefaultProfile</span></span>
<span data-ttu-id="ea459-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea459-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea459-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ea459-113">-Name</span></span>
<span data-ttu-id="ea459-114">Nome do Registro de destino.</span><span class="sxs-lookup"><span data-stu-id="ea459-114">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea459-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea459-115">-ResourceGroupName</span></span>
<span data-ttu-id="ea459-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ea459-116">Resource group name.</span></span>

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

### <span data-ttu-id="ea459-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea459-117">CommonParameters</span></span>
<span data-ttu-id="ea459-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea459-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea459-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea459-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea459-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea459-120">INPUTS</span></span>

### <span data-ttu-id="ea459-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ea459-121">System.String</span></span>

## <span data-ttu-id="ea459-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ea459-122">OUTPUTS</span></span>

### <span data-ttu-id="ea459-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="ea459-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="ea459-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="ea459-124">NOTES</span></span>

## <span data-ttu-id="ea459-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea459-125">RELATED LINKS</span></span>
