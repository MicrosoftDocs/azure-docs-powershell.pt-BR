---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: e7d84439b2292d70604f3f7d9e827a0d8cc035e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434127"
---
# <span data-ttu-id="bf614-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="bf614-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="bf614-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf614-102">SYNOPSIS</span></span>
<span data-ttu-id="bf614-103">Obtenha o uso de um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf614-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="bf614-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf614-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf614-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf614-105">DESCRIPTION</span></span>
<span data-ttu-id="bf614-106">Obtenha o uso de um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf614-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="bf614-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf614-107">EXAMPLES</span></span>

### <span data-ttu-id="bf614-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf614-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="bf614-109">Obtenha o uso de um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf614-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="bf614-110">OS</span><span class="sxs-lookup"><span data-stu-id="bf614-110">PARAMETERS</span></span>

### <span data-ttu-id="bf614-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf614-111">-DefaultProfile</span></span>
<span data-ttu-id="bf614-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf614-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf614-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf614-113">-Name</span></span>
<span data-ttu-id="bf614-114">Nome do registro de destino.</span><span class="sxs-lookup"><span data-stu-id="bf614-114">Target registry name.</span></span>

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

### <span data-ttu-id="bf614-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf614-115">-ResourceGroupName</span></span>
<span data-ttu-id="bf614-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bf614-116">Resource group name.</span></span>

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

### <span data-ttu-id="bf614-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf614-117">CommonParameters</span></span>
<span data-ttu-id="bf614-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf614-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf614-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf614-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf614-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf614-120">INPUTS</span></span>

### <span data-ttu-id="bf614-121">System. String</span><span class="sxs-lookup"><span data-stu-id="bf614-121">System.String</span></span>

## <span data-ttu-id="bf614-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf614-122">OUTPUTS</span></span>

### <span data-ttu-id="bf614-123">Microsoft. Azure. Commands. ContainerRegistry. Models. PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="bf614-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="bf614-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf614-124">NOTES</span></span>

## <span data-ttu-id="bf614-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf614-125">RELATED LINKS</span></span>
