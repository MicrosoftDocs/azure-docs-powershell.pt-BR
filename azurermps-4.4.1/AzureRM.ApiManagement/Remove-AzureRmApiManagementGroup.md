---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
ms.openlocfilehash: 6a866932d5fa46c621e4ac67e5147650dc1dbc28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428319"
---
# <span data-ttu-id="e0ecf-101">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e0ecf-101">Remove-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="e0ecf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ecf-103">Remove um grupo de gerenciamento de APIs existente.</span><span class="sxs-lookup"><span data-stu-id="e0ecf-103">Removes an existing API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0ecf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0ecf-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0ecf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="e0ecf-106">O cmdlet **Remove-AzureRmApiManagementGroup** remove um grupo de gerenciamento de API existente.</span><span class="sxs-lookup"><span data-stu-id="e0ecf-106">The **Remove-AzureRmApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="e0ecf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0ecf-107">EXAMPLES</span></span>

### <span data-ttu-id="e0ecf-108">Exemplo 1: remover um grupo de gerenciamento existente</span><span class="sxs-lookup"><span data-stu-id="e0ecf-108">Example 1: Remove an existing management group</span></span>
```
PS C:\>Remove-AzureRmApiManagementGroup -Context $APImContext -GroupId "Group0001" -Force
```

<span data-ttu-id="e0ecf-109">Esse comando Remove um grupo de gerenciamento existente chamado Group0001 e não solicita que o usuário confirme.</span><span class="sxs-lookup"><span data-stu-id="e0ecf-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="e0ecf-110">OS</span><span class="sxs-lookup"><span data-stu-id="e0ecf-110">PARAMETERS</span></span>

### <span data-ttu-id="e0ecf-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e0ecf-111">-Context</span></span>
<span data-ttu-id="e0ecf-112">Especifica a instância de um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e0ecf-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e0ecf-113">-GroupId</span><span class="sxs-lookup"><span data-stu-id="e0ecf-113">-GroupId</span></span>
<span data-ttu-id="e0ecf-114">Especifica o identificador de um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="e0ecf-114">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="e0ecf-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0ecf-115">-PassThru</span></span>
<span data-ttu-id="e0ecf-116">Indica que esse cmdlet retorna um valor de $True se tiver êxito ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="e0ecf-116">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="e0ecf-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e0ecf-117">-Confirm</span></span>
<span data-ttu-id="e0ecf-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0ecf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0ecf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0ecf-119">-WhatIf</span></span>
<span data-ttu-id="e0ecf-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0ecf-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0ecf-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0ecf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0ecf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ecf-122">-DefaultProfile</span></span>
<span data-ttu-id="e0ecf-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ecf-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0ecf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ecf-124">CommonParameters</span></span>
<span data-ttu-id="e0ecf-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0ecf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ecf-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0ecf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ecf-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0ecf-127">INPUTS</span></span>

## <span data-ttu-id="e0ecf-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0ecf-128">OUTPUTS</span></span>

### <span data-ttu-id="e0ecf-129">Booliana</span><span class="sxs-lookup"><span data-stu-id="e0ecf-129">Boolean</span></span>

## <span data-ttu-id="e0ecf-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0ecf-130">NOTES</span></span>

## <span data-ttu-id="e0ecf-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0ecf-131">RELATED LINKS</span></span>

[<span data-ttu-id="e0ecf-132">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e0ecf-132">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="e0ecf-133">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e0ecf-133">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="e0ecf-134">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e0ecf-134">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


