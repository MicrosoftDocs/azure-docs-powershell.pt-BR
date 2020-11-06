---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 766682df23beaa7c513ff54554a3ebd59a6d1537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440591"
---
# <span data-ttu-id="07cda-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="07cda-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="07cda-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07cda-102">SYNOPSIS</span></span>
<span data-ttu-id="07cda-103">Redefine a tecla de acesso especificada.</span><span class="sxs-lookup"><span data-stu-id="07cda-103">Resets the specified access key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07cda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07cda-104">SYNTAX</span></span>

```
Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07cda-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07cda-105">DESCRIPTION</span></span>
<span data-ttu-id="07cda-106">O cmdlet **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** redefine a tecla de acesso especificada em seu conjunto do espaço de trabalho do Power bi.</span><span class="sxs-lookup"><span data-stu-id="07cda-106">The **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="07cda-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07cda-107">EXAMPLES</span></span>

### <span data-ttu-id="07cda-108">Exemplo 1: redefinir a chave de acesso principal</span><span class="sxs-lookup"><span data-stu-id="07cda-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="07cda-109">Esse comando redefine a chave de acesso principal para a coleção de espaço de trabalho chamada WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="07cda-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="07cda-110">OS</span><span class="sxs-lookup"><span data-stu-id="07cda-110">PARAMETERS</span></span>

### <span data-ttu-id="07cda-111">-Key1</span><span class="sxs-lookup"><span data-stu-id="07cda-111">-Key1</span></span>
<span data-ttu-id="07cda-112">Indica que esse cmdlet redefine a chave de acesso principal.</span><span class="sxs-lookup"><span data-stu-id="07cda-112">Indicates that this cmdlet resets the primary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cda-113">-Key2</span><span class="sxs-lookup"><span data-stu-id="07cda-113">-Key2</span></span>
<span data-ttu-id="07cda-114">Indica que esse cmdlet redefine a chave de acesso secundário.</span><span class="sxs-lookup"><span data-stu-id="07cda-114">Indicates that this cmdlet resets the secondary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cda-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07cda-115">-ResourceGroupName</span></span>
<span data-ttu-id="07cda-116">Especifica o nome do grupo de recursos da coleção.</span><span class="sxs-lookup"><span data-stu-id="07cda-116">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="07cda-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="07cda-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="07cda-118">Especifica o nome da coleção do espaço de trabalho do Power BI na qual esse cmdlet funciona.</span><span class="sxs-lookup"><span data-stu-id="07cda-118">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07cda-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="07cda-119">-Confirm</span></span>
<span data-ttu-id="07cda-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07cda-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cda-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07cda-121">-WhatIf</span></span>
<span data-ttu-id="07cda-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07cda-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07cda-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07cda-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cda-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07cda-124">-DefaultProfile</span></span>
<span data-ttu-id="07cda-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07cda-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07cda-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07cda-126">CommonParameters</span></span>
<span data-ttu-id="07cda-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07cda-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07cda-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07cda-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07cda-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07cda-129">INPUTS</span></span>

## <span data-ttu-id="07cda-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07cda-130">OUTPUTS</span></span>

### <span data-ttu-id="07cda-131">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="07cda-131">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="07cda-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07cda-132">NOTES</span></span>

## <span data-ttu-id="07cda-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07cda-133">RELATED LINKS</span></span>

[<span data-ttu-id="07cda-134">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="07cda-134">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


