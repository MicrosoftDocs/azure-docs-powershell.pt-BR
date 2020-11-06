---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: b4e1a029eca4e7eda48f44d85292639767eaf845
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432693"
---
# <span data-ttu-id="cd1a2-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="cd1a2-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="cd1a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="cd1a2-103">Adiciona um produto a um grupo.</span><span class="sxs-lookup"><span data-stu-id="cd1a2-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd1a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd1a2-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd1a2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd1a2-105">DESCRIPTION</span></span>
<span data-ttu-id="cd1a2-106">O cmdlet **Add-AzureRmApiManagementProductToGroup** adiciona um produto a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="cd1a2-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="cd1a2-107">Em outras palavras, esse cmdlet atribui um grupo a um produto.</span><span class="sxs-lookup"><span data-stu-id="cd1a2-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="cd1a2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd1a2-108">EXAMPLES</span></span>

### <span data-ttu-id="cd1a2-109">Exemplo 1: adicionar um produto a um grupo</span><span class="sxs-lookup"><span data-stu-id="cd1a2-109">Example 1: Add a product to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="cd1a2-110">Esse comando adiciona um produto a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="cd1a2-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="cd1a2-111">OS</span><span class="sxs-lookup"><span data-stu-id="cd1a2-111">PARAMETERS</span></span>

### <span data-ttu-id="cd1a2-112">-Contexto</span><span class="sxs-lookup"><span data-stu-id="cd1a2-112">-Context</span></span>
<span data-ttu-id="cd1a2-113">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cd1a2-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="cd1a2-114">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="cd1a2-114">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd1a2-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="cd1a2-115">-GroupId</span></span>
<span data-ttu-id="cd1a2-116">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="cd1a2-116">Specifies the group ID.</span></span>
<span data-ttu-id="cd1a2-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="cd1a2-117">This parameter is required.</span></span>

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

### <span data-ttu-id="cd1a2-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd1a2-118">-PassThru</span></span>
<span data-ttu-id="cd1a2-119">PassThru</span><span class="sxs-lookup"><span data-stu-id="cd1a2-119">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd1a2-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="cd1a2-120">-ProductId</span></span>
<span data-ttu-id="cd1a2-121">Especifica a ID do produto.</span><span class="sxs-lookup"><span data-stu-id="cd1a2-121">Specifies the product ID.</span></span>
<span data-ttu-id="cd1a2-122">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="cd1a2-122">This parameter is required.</span></span>

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

### <span data-ttu-id="cd1a2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd1a2-123">-DefaultProfile</span></span>
<span data-ttu-id="cd1a2-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd1a2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd1a2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd1a2-125">CommonParameters</span></span>
<span data-ttu-id="cd1a2-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd1a2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd1a2-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd1a2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd1a2-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd1a2-128">INPUTS</span></span>

## <span data-ttu-id="cd1a2-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd1a2-129">OUTPUTS</span></span>

### <span data-ttu-id="cd1a2-130">Booliana</span><span class="sxs-lookup"><span data-stu-id="cd1a2-130">Boolean</span></span>

## <span data-ttu-id="cd1a2-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd1a2-131">NOTES</span></span>

## <span data-ttu-id="cd1a2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd1a2-132">RELATED LINKS</span></span>

[<span data-ttu-id="cd1a2-133">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="cd1a2-133">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


