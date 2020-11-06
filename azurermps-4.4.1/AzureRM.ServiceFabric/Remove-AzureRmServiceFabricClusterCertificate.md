---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 0ef59a8071438fa1bfd1560ab2f2102722aa335f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429093"
---
# <span data-ttu-id="2c4c2-101">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2c4c2-101">Remove-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="2c4c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c4c2-102">SYNOPSIS</span></span>
<span data-ttu-id="2c4c2-103">Remover um certificado de cluster de ser usado para a segurança do cluster.</span><span class="sxs-lookup"><span data-stu-id="2c4c2-103">Remove a cluster certificate from being used for cluster security.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c4c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c4c2-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c4c2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c4c2-105">DESCRIPTION</span></span>
<span data-ttu-id="2c4c2-106">Use **Remove-AzureRmServiceFabricClusterCertificate** para remover um certificado de cluster do cluster, contanto que haja outro certificado válido que já esteja em uso no cluster.</span><span class="sxs-lookup"><span data-stu-id="2c4c2-106">Use **Remove-AzureRmServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="2c4c2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c4c2-107">EXAMPLES</span></span>

### <span data-ttu-id="2c4c2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c4c2-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="2c4c2-109">Esse comando Remove o certificado com a impressão digital 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A de ser usado para a segurança do cluster.</span><span class="sxs-lookup"><span data-stu-id="2c4c2-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="2c4c2-110">OS</span><span class="sxs-lookup"><span data-stu-id="2c4c2-110">PARAMETERS</span></span>

### <span data-ttu-id="2c4c2-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c4c2-111">-Name</span></span>
<span data-ttu-id="2c4c2-112">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="2c4c2-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2c4c2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c4c2-113">-ResourceGroupName</span></span>
<span data-ttu-id="2c4c2-114">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c4c2-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2c4c2-115">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="2c4c2-115">-Thumbprint</span></span>
<span data-ttu-id="2c4c2-116">Especifique a impressão digital do cluster que será removida.</span><span class="sxs-lookup"><span data-stu-id="2c4c2-116">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="2c4c2-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c4c2-117">-Confirm</span></span>
<span data-ttu-id="2c4c2-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c4c2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c4c2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c4c2-119">-WhatIf</span></span>
<span data-ttu-id="2c4c2-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c4c2-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c4c2-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c4c2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c4c2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c4c2-122">-DefaultProfile</span></span>
<span data-ttu-id="2c4c2-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c4c2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c4c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c4c2-124">CommonParameters</span></span>
<span data-ttu-id="2c4c2-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c4c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c4c2-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c4c2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c4c2-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c4c2-127">INPUTS</span></span>

### <span data-ttu-id="2c4c2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2c4c2-128">System.String</span></span>

## <span data-ttu-id="2c4c2-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c4c2-129">OUTPUTS</span></span>

### <span data-ttu-id="2c4c2-130">Microsoft. Azure. Commands. imfabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="2c4c2-130">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="2c4c2-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c4c2-131">NOTES</span></span>

## <span data-ttu-id="2c4c2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c4c2-132">RELATED LINKS</span></span>

