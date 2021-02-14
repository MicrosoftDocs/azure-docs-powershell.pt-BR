---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116688"
---
# <span data-ttu-id="12adb-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="12adb-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="12adb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12adb-102">SYNOPSIS</span></span>
<span data-ttu-id="12adb-103">Clusters gerenciados pela List List List.</span><span class="sxs-lookup"><span data-stu-id="12adb-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="12adb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12adb-104">SYNTAX</span></span>

### <span data-ttu-id="12adb-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="12adb-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12adb-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12adb-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12adb-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="12adb-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12adb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="12adb-108">DESCRIPTION</span></span>
<span data-ttu-id="12adb-109">Clusters gerenciados da Lista de ListAgem.</span><span class="sxs-lookup"><span data-stu-id="12adb-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="12adb-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="12adb-110">EXAMPLES</span></span>

### <span data-ttu-id="12adb-111">Listar todos os clusters de ListAgemnetes</span><span class="sxs-lookup"><span data-stu-id="12adb-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="12adb-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12adb-112">PARAMETERS</span></span>

### <span data-ttu-id="12adb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12adb-113">-DefaultProfile</span></span>
<span data-ttu-id="12adb-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12adb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12adb-115">-ID</span><span class="sxs-lookup"><span data-stu-id="12adb-115">-Id</span></span>
<span data-ttu-id="12adb-116">ID de um cluster de Redenetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="12adb-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12adb-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="12adb-117">-Name</span></span>
<span data-ttu-id="12adb-118">Nome do cluster Desarnetes gerenciados</span><span class="sxs-lookup"><span data-stu-id="12adb-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12adb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12adb-119">-ResourceGroupName</span></span>
<span data-ttu-id="12adb-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="12adb-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12adb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12adb-121">CommonParameters</span></span>
<span data-ttu-id="12adb-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12adb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12adb-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12adb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12adb-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="12adb-124">INPUTS</span></span>

### <span data-ttu-id="12adb-125">System.String</span><span class="sxs-lookup"><span data-stu-id="12adb-125">System.String</span></span>

## <span data-ttu-id="12adb-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="12adb-126">OUTPUTS</span></span>

### <span data-ttu-id="12adb-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="12adb-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="12adb-128">Notas</span><span class="sxs-lookup"><span data-stu-id="12adb-128">NOTES</span></span>

## <span data-ttu-id="12adb-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12adb-129">RELATED LINKS</span></span>
