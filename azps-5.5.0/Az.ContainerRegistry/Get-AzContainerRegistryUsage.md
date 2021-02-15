---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: e7d84439b2292d70604f3f7d9e827a0d8cc035e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112085"
---
# <span data-ttu-id="fb6df-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="fb6df-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="fb6df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb6df-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6df-103">Obter o Uso de um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb6df-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="fb6df-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb6df-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb6df-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb6df-105">DESCRIPTION</span></span>
<span data-ttu-id="fb6df-106">Obter o Uso de um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb6df-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="fb6df-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fb6df-107">EXAMPLES</span></span>

### <span data-ttu-id="fb6df-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb6df-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="fb6df-109">Obter o Uso de um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb6df-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="fb6df-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb6df-110">PARAMETERS</span></span>

### <span data-ttu-id="fb6df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6df-111">-DefaultProfile</span></span>
<span data-ttu-id="fb6df-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb6df-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb6df-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb6df-113">-Name</span></span>
<span data-ttu-id="fb6df-114">Nome do registro de destino.</span><span class="sxs-lookup"><span data-stu-id="fb6df-114">Target registry name.</span></span>

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

### <span data-ttu-id="fb6df-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb6df-115">-ResourceGroupName</span></span>
<span data-ttu-id="fb6df-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fb6df-116">Resource group name.</span></span>

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

### <span data-ttu-id="fb6df-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6df-117">CommonParameters</span></span>
<span data-ttu-id="fb6df-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb6df-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6df-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb6df-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6df-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="fb6df-120">INPUTS</span></span>

### <span data-ttu-id="fb6df-121">System.String</span><span class="sxs-lookup"><span data-stu-id="fb6df-121">System.String</span></span>

## <span data-ttu-id="fb6df-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="fb6df-122">OUTPUTS</span></span>

### <span data-ttu-id="fb6df-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="fb6df-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="fb6df-124">Notas</span><span class="sxs-lookup"><span data-stu-id="fb6df-124">NOTES</span></span>

## <span data-ttu-id="fb6df-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb6df-125">RELATED LINKS</span></span>
