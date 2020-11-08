---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 691d8cf006e720d706d2473f76ff8660927e73ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115582"
---
# <span data-ttu-id="bb95e-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="bb95e-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="bb95e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb95e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb95e-103">Obtenha o uso de um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb95e-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="bb95e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb95e-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb95e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb95e-105">DESCRIPTION</span></span>
<span data-ttu-id="bb95e-106">Obtenha o uso de um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb95e-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="bb95e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb95e-107">EXAMPLES</span></span>

### <span data-ttu-id="bb95e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb95e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="bb95e-109">Obtenha o uso de um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb95e-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="bb95e-110">OS</span><span class="sxs-lookup"><span data-stu-id="bb95e-110">PARAMETERS</span></span>

### <span data-ttu-id="bb95e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb95e-111">-DefaultProfile</span></span>
<span data-ttu-id="bb95e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb95e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb95e-113">-Registryname</span><span class="sxs-lookup"><span data-stu-id="bb95e-113">-RegistryName</span></span>
<span data-ttu-id="bb95e-114">Nome do registro de destino.</span><span class="sxs-lookup"><span data-stu-id="bb95e-114">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb95e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb95e-115">-ResourceGroupName</span></span>
<span data-ttu-id="bb95e-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb95e-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb95e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb95e-117">CommonParameters</span></span>
<span data-ttu-id="bb95e-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb95e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb95e-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb95e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb95e-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb95e-120">INPUTS</span></span>

### <span data-ttu-id="bb95e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="bb95e-121">System.String</span></span>

## <span data-ttu-id="bb95e-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb95e-122">OUTPUTS</span></span>

### <span data-ttu-id="bb95e-123">Microsoft. Azure. Commands. ContainerRegistry. Models. PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="bb95e-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="bb95e-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb95e-124">NOTES</span></span>

## <span data-ttu-id="bb95e-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb95e-125">RELATED LINKS</span></span>
