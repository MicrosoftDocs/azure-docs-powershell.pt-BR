---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: e7d84439b2292d70604f3f7d9e827a0d8cc035e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257931"
---
# <span data-ttu-id="f9b9c-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="f9b9c-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="f9b9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b9c-103">Obtenha o uso de um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9b9c-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="f9b9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9b9c-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9b9c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="f9b9c-106">Obtenha o uso de um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9b9c-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="f9b9c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9b9c-107">EXAMPLES</span></span>

### <span data-ttu-id="f9b9c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f9b9c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="f9b9c-109">Obtenha o uso de um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9b9c-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="f9b9c-110">OS</span><span class="sxs-lookup"><span data-stu-id="f9b9c-110">PARAMETERS</span></span>

### <span data-ttu-id="f9b9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b9c-111">-DefaultProfile</span></span>
<span data-ttu-id="f9b9c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9b9c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9b9c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9b9c-113">-Name</span></span>
<span data-ttu-id="f9b9c-114">Nome do registro de destino.</span><span class="sxs-lookup"><span data-stu-id="f9b9c-114">Target registry name.</span></span>

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

### <span data-ttu-id="f9b9c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b9c-115">-ResourceGroupName</span></span>
<span data-ttu-id="f9b9c-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9b9c-116">Resource group name.</span></span>

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

### <span data-ttu-id="f9b9c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b9c-117">CommonParameters</span></span>
<span data-ttu-id="f9b9c-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9b9c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b9c-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9b9c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b9c-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9b9c-120">INPUTS</span></span>

### <span data-ttu-id="f9b9c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f9b9c-121">System.String</span></span>

## <span data-ttu-id="f9b9c-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9b9c-122">OUTPUTS</span></span>

### <span data-ttu-id="f9b9c-123">Microsoft. Azure. Commands. ContainerRegistry. Models. PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="f9b9c-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="f9b9c-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9b9c-124">NOTES</span></span>

## <span data-ttu-id="f9b9c-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9b9c-125">RELATED LINKS</span></span>
