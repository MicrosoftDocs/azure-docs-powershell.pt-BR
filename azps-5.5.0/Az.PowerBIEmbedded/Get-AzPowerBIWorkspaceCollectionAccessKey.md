---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 9108f224297b23fd391e1a4c3afac4b826aa3dbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112705"
---
# <span data-ttu-id="40fe4-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="40fe4-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="40fe4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="40fe4-103">Obtém as chaves de acesso atuais associadas a um conjunto de espaços de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="40fe4-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="40fe4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40fe4-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40fe4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="40fe4-105">DESCRIPTION</span></span>
<span data-ttu-id="40fe4-106">O cmdlet **Get-AzPowerBIWorkspaceCollectionAccessKey** obtém as chaves de acesso atuais associadas a um conjunto de espaços de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="40fe4-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="40fe4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="40fe4-107">EXAMPLES</span></span>

### <span data-ttu-id="40fe4-108">Exemplo 1: Obter teclas de acesso</span><span class="sxs-lookup"><span data-stu-id="40fe4-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="40fe4-109">Esse comando obtém chaves de acesso para o conjunto de espaços de trabalho chamado WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="40fe4-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="40fe4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40fe4-110">PARAMETERS</span></span>

### <span data-ttu-id="40fe4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40fe4-111">-DefaultProfile</span></span>
<span data-ttu-id="40fe4-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="40fe4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40fe4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40fe4-113">-ResourceGroupName</span></span>
<span data-ttu-id="40fe4-114">Especifica o nome do grupo de recursos da coleção.</span><span class="sxs-lookup"><span data-stu-id="40fe4-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="40fe4-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="40fe4-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="40fe4-116">Especifica o nome do conjunto de espaços de trabalho do Power BI no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="40fe4-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="40fe4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40fe4-117">CommonParameters</span></span>
<span data-ttu-id="40fe4-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40fe4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40fe4-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40fe4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40fe4-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="40fe4-120">INPUTS</span></span>

### <span data-ttu-id="40fe4-121">System.String</span><span class="sxs-lookup"><span data-stu-id="40fe4-121">System.String</span></span>

## <span data-ttu-id="40fe4-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="40fe4-122">OUTPUTS</span></span>

### <span data-ttu-id="40fe4-123">Microsoft.Azure.Commands.Management.PowerBIEmbekey.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="40fe4-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="40fe4-124">Notas</span><span class="sxs-lookup"><span data-stu-id="40fe4-124">NOTES</span></span>

## <span data-ttu-id="40fe4-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40fe4-125">RELATED LINKS</span></span>

[<span data-ttu-id="40fe4-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="40fe4-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


