---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 59f8723470707a644e426bd9559a8e982f731e6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892342"
---
# <span data-ttu-id="a16d7-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a16d7-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="a16d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a16d7-102">SYNOPSIS</span></span>
<span data-ttu-id="a16d7-103">Remova um certificado de cluster de ser usado para segurança de cluster.</span><span class="sxs-lookup"><span data-stu-id="a16d7-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="a16d7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a16d7-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a16d7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a16d7-105">DESCRIPTION</span></span>
<span data-ttu-id="a16d7-106">Use **Remove-AzServiceFabricClusterCertificate** para remover um certificado de cluster do cluster, desde que haja outro certificado válido que já está em uso no cluster.</span><span class="sxs-lookup"><span data-stu-id="a16d7-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="a16d7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a16d7-107">EXAMPLES</span></span>

### <span data-ttu-id="a16d7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a16d7-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="a16d7-109">Este comando remove o certificado com a impressão digital 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A de ser usada para segurança de cluster.</span><span class="sxs-lookup"><span data-stu-id="a16d7-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="a16d7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a16d7-110">PARAMETERS</span></span>

### <span data-ttu-id="a16d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a16d7-111">-DefaultProfile</span></span>
<span data-ttu-id="a16d7-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a16d7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a16d7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a16d7-113">-Name</span></span>
<span data-ttu-id="a16d7-114">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a16d7-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a16d7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a16d7-115">-ResourceGroupName</span></span>
<span data-ttu-id="a16d7-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a16d7-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a16d7-117">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="a16d7-117">-Thumbprint</span></span>
<span data-ttu-id="a16d7-118">Especifique a impressão digital do cluster a ser removida.</span><span class="sxs-lookup"><span data-stu-id="a16d7-118">Specify the cluster thumbprint which to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a16d7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a16d7-119">-Confirm</span></span>
<span data-ttu-id="a16d7-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a16d7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a16d7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a16d7-121">-WhatIf</span></span>
<span data-ttu-id="a16d7-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a16d7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a16d7-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a16d7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a16d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a16d7-124">CommonParameters</span></span>
<span data-ttu-id="a16d7-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a16d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a16d7-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a16d7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a16d7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a16d7-127">INPUTS</span></span>

### <span data-ttu-id="a16d7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a16d7-128">System.String</span></span>

## <span data-ttu-id="a16d7-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a16d7-129">OUTPUTS</span></span>

### <span data-ttu-id="a16d7-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="a16d7-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a16d7-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="a16d7-131">NOTES</span></span>

## <span data-ttu-id="a16d7-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a16d7-132">RELATED LINKS</span></span>
