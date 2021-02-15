---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 688ee9f8679a427d53319147e7d13fc9e1305277
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116174"
---
# <span data-ttu-id="4b402-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="4b402-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="4b402-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b402-102">SYNOPSIS</span></span>
<span data-ttu-id="4b402-103">Remova um certificado de cluster de ser usado para segurança de cluster.</span><span class="sxs-lookup"><span data-stu-id="4b402-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="4b402-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b402-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b402-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b402-105">DESCRIPTION</span></span>
<span data-ttu-id="4b402-106">Use **Remove-AzServiceFabricClusterCertificate** para remover um certificado de cluster do cluster, desde que haja outro certificado válido que já está em uso no cluster.</span><span class="sxs-lookup"><span data-stu-id="4b402-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="4b402-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4b402-107">EXAMPLES</span></span>

### <span data-ttu-id="4b402-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b402-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="4b402-109">Esse comando remove o certificado com a impressão de miniatura 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A de ser usado para segurança de cluster.</span><span class="sxs-lookup"><span data-stu-id="4b402-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="4b402-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b402-110">PARAMETERS</span></span>

### <span data-ttu-id="4b402-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b402-111">-DefaultProfile</span></span>
<span data-ttu-id="4b402-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4b402-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b402-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b402-113">-Name</span></span>
<span data-ttu-id="4b402-114">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="4b402-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4b402-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b402-115">-ResourceGroupName</span></span>
<span data-ttu-id="4b402-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b402-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4b402-117">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="4b402-117">-Thumbprint</span></span>
<span data-ttu-id="4b402-118">Especifique a impressão digital de cluster que deve ser removida.</span><span class="sxs-lookup"><span data-stu-id="4b402-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="4b402-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4b402-119">-Confirm</span></span>
<span data-ttu-id="4b402-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b402-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b402-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b402-121">-WhatIf</span></span>
<span data-ttu-id="4b402-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4b402-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b402-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b402-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b402-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b402-124">CommonParameters</span></span>
<span data-ttu-id="4b402-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b402-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b402-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b402-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b402-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="4b402-127">INPUTS</span></span>

### <span data-ttu-id="4b402-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4b402-128">System.String</span></span>

## <span data-ttu-id="4b402-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="4b402-129">OUTPUTS</span></span>

### <span data-ttu-id="4b402-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="4b402-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="4b402-131">Notas</span><span class="sxs-lookup"><span data-stu-id="4b402-131">NOTES</span></span>

## <span data-ttu-id="4b402-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b402-132">RELATED LINKS</span></span>
