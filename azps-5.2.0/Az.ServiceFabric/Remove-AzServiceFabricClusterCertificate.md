---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 688ee9f8679a427d53319147e7d13fc9e1305277
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261510"
---
# <span data-ttu-id="597e8-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="597e8-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="597e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="597e8-102">SYNOPSIS</span></span>
<span data-ttu-id="597e8-103">Remover um certificado de cluster de ser usado para a segurança do cluster.</span><span class="sxs-lookup"><span data-stu-id="597e8-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="597e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="597e8-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="597e8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="597e8-105">DESCRIPTION</span></span>
<span data-ttu-id="597e8-106">Use **Remove-AzServiceFabricClusterCertificate** para remover um certificado de cluster do cluster, contanto que haja outro certificado válido que já esteja em uso no cluster.</span><span class="sxs-lookup"><span data-stu-id="597e8-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="597e8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="597e8-107">EXAMPLES</span></span>

### <span data-ttu-id="597e8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="597e8-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="597e8-109">Esse comando Remove o certificado com a impressão digital 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A de ser usado para a segurança do cluster.</span><span class="sxs-lookup"><span data-stu-id="597e8-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="597e8-110">OS</span><span class="sxs-lookup"><span data-stu-id="597e8-110">PARAMETERS</span></span>

### <span data-ttu-id="597e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="597e8-111">-DefaultProfile</span></span>
<span data-ttu-id="597e8-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="597e8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="597e8-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="597e8-113">-Name</span></span>
<span data-ttu-id="597e8-114">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="597e8-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="597e8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="597e8-115">-ResourceGroupName</span></span>
<span data-ttu-id="597e8-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="597e8-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="597e8-117">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="597e8-117">-Thumbprint</span></span>
<span data-ttu-id="597e8-118">Especifique a impressão digital do cluster que será removida.</span><span class="sxs-lookup"><span data-stu-id="597e8-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="597e8-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="597e8-119">-Confirm</span></span>
<span data-ttu-id="597e8-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="597e8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="597e8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="597e8-121">-WhatIf</span></span>
<span data-ttu-id="597e8-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="597e8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="597e8-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="597e8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="597e8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="597e8-124">CommonParameters</span></span>
<span data-ttu-id="597e8-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="597e8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="597e8-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="597e8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="597e8-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="597e8-127">INPUTS</span></span>

### <span data-ttu-id="597e8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="597e8-128">System.String</span></span>

## <span data-ttu-id="597e8-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="597e8-129">OUTPUTS</span></span>

### <span data-ttu-id="597e8-130">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="597e8-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="597e8-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="597e8-131">NOTES</span></span>

## <span data-ttu-id="597e8-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="597e8-132">RELATED LINKS</span></span>
