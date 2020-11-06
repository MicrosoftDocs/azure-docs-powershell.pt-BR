---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: c3a783178bf8342e891f8eab2996e77a2045721a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609496"
---
# <span data-ttu-id="adf27-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="adf27-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="adf27-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="adf27-102">SYNOPSIS</span></span>
<span data-ttu-id="adf27-103">Obter membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="adf27-103">Get a group members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adf27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="adf27-104">SYNTAX</span></span>

```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="adf27-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="adf27-105">DESCRIPTION</span></span>
<span data-ttu-id="adf27-106">Obter membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="adf27-106">Get a group members.</span></span>

## <span data-ttu-id="adf27-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="adf27-107">EXAMPLES</span></span>

### <span data-ttu-id="adf27-108">Filtrar membros do grupo usando a ID do objeto de grupo</span><span class="sxs-lookup"><span data-stu-id="adf27-108">Filters group members using group object id</span></span>
```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="adf27-109">Obtém membros do grupo com a ID 85F89C90-780E-4AA6-9F4F-6F268D322EEE</span><span class="sxs-lookup"><span data-stu-id="adf27-109">Gets group members with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

## <span data-ttu-id="adf27-110">OS</span><span class="sxs-lookup"><span data-stu-id="adf27-110">PARAMETERS</span></span>

### <span data-ttu-id="adf27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adf27-111">-DefaultProfile</span></span>
<span data-ttu-id="adf27-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="adf27-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf27-113">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="adf27-113">-GroupObjectId</span></span>
<span data-ttu-id="adf27-114">ID de objeto do grupo.</span><span class="sxs-lookup"><span data-stu-id="adf27-114">Object id of the group.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adf27-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adf27-115">CommonParameters</span></span>
<span data-ttu-id="adf27-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adf27-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adf27-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adf27-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adf27-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="adf27-118">INPUTS</span></span>

### <span data-ttu-id="adf27-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="adf27-119">None</span></span>
<span data-ttu-id="adf27-120">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="adf27-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="adf27-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="adf27-121">OUTPUTS</span></span>

### <span data-ttu-id="adf27-122">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject]</span><span class="sxs-lookup"><span data-stu-id="adf27-122">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject]</span></span>

## <span data-ttu-id="adf27-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="adf27-123">NOTES</span></span>

## <span data-ttu-id="adf27-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adf27-124">RELATED LINKS</span></span>

[<span data-ttu-id="adf27-125">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="adf27-125">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="adf27-126">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="adf27-126">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

