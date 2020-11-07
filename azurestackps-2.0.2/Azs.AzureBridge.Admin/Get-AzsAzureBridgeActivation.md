---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d47f93addf05af19b523db6ba454443af2c34f
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2020
ms.locfileid: "93947323"
---
# <span data-ttu-id="3adeb-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="3adeb-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="3adeb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3adeb-102">SYNOPSIS</span></span>
<span data-ttu-id="3adeb-103">Retorna a ativação da ponte do Azure.</span><span class="sxs-lookup"><span data-stu-id="3adeb-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="3adeb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3adeb-104">SYNTAX</span></span>

### <span data-ttu-id="3adeb-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="3adeb-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3adeb-106">Obter</span><span class="sxs-lookup"><span data-stu-id="3adeb-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="3adeb-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="3adeb-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3adeb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3adeb-108">DESCRIPTION</span></span>
<span data-ttu-id="3adeb-109">Depois que o Azure Stack for registrado, o objeto de ativação contém informações que vinculam uma implantação de pilha do Azure ao seu registro no Azure, por exemplo, a data de expiração de registro, o nome, etc.</span><span class="sxs-lookup"><span data-stu-id="3adeb-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="3adeb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3adeb-110">EXAMPLES</span></span>

### <span data-ttu-id="3adeb-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3adeb-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="3adeb-112">Obter uma lista de ativações de ponte do Azure no grupo de recursos "activationRG"</span><span class="sxs-lookup"><span data-stu-id="3adeb-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="3adeb-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3adeb-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="3adeb-114">Obter uma ativação do Azure Bridge por nome ' myactivationting ' situado em ' activationRG '</span><span class="sxs-lookup"><span data-stu-id="3adeb-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="3adeb-115">OS</span><span class="sxs-lookup"><span data-stu-id="3adeb-115">PARAMETERS</span></span>

### <span data-ttu-id="3adeb-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3adeb-116">-Name</span></span>
<span data-ttu-id="3adeb-117">Nome da ativação.</span><span class="sxs-lookup"><span data-stu-id="3adeb-117">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3adeb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3adeb-118">-ResourceGroupName</span></span>
<span data-ttu-id="3adeb-119">O grupo de recursos usado durante o registro do Azure Stack; Você também pode exibir nomes de grupo de recursos no Portal.</span><span class="sxs-lookup"><span data-stu-id="3adeb-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3adeb-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3adeb-120">-ResourceId</span></span>
<span data-ttu-id="3adeb-121">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="3adeb-121">The resource id.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3adeb-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="3adeb-122">-Skip</span></span>
<span data-ttu-id="3adeb-123">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3adeb-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3adeb-124">-Início</span><span class="sxs-lookup"><span data-stu-id="3adeb-124">-Top</span></span>
<span data-ttu-id="3adeb-125">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3adeb-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3adeb-126">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="3adeb-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3adeb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3adeb-127">CommonParameters</span></span>
<span data-ttu-id="3adeb-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3adeb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3adeb-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3adeb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3adeb-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3adeb-130">INPUTS</span></span>

## <span data-ttu-id="3adeb-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3adeb-131">OUTPUTS</span></span>

### <span data-ttu-id="3adeb-132">Microsoft. AzureStack. Management. AzureBridge. admin. Models. ActivationResource</span><span class="sxs-lookup"><span data-stu-id="3adeb-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="3adeb-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3adeb-133">NOTES</span></span>

## <span data-ttu-id="3adeb-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3adeb-134">RELATED LINKS</span></span>

