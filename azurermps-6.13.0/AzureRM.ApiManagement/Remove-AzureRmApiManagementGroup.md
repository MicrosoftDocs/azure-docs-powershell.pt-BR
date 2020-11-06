---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
ms.openlocfilehash: d297c4f8bb9999d60ec694c73aa723dd4afec58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426492"
---
# <span data-ttu-id="15202-101">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="15202-101">Remove-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="15202-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15202-102">SYNOPSIS</span></span>
<span data-ttu-id="15202-103">Remove um grupo de gerenciamento de APIs existente.</span><span class="sxs-lookup"><span data-stu-id="15202-103">Removes an existing API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15202-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15202-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15202-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15202-105">DESCRIPTION</span></span>
<span data-ttu-id="15202-106">O cmdlet **Remove-AzureRmApiManagementGroup** remove um grupo de gerenciamento de API existente.</span><span class="sxs-lookup"><span data-stu-id="15202-106">The **Remove-AzureRmApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="15202-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15202-107">EXAMPLES</span></span>

### <span data-ttu-id="15202-108">Exemplo 1: remover um grupo de gerenciamento existente</span><span class="sxs-lookup"><span data-stu-id="15202-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="15202-109">Esse comando Remove um grupo de gerenciamento existente chamado Group0001 e não solicita que o usuário confirme.</span><span class="sxs-lookup"><span data-stu-id="15202-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="15202-110">OS</span><span class="sxs-lookup"><span data-stu-id="15202-110">PARAMETERS</span></span>

### <span data-ttu-id="15202-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="15202-111">-Context</span></span>
<span data-ttu-id="15202-112">Especifica a instância de um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="15202-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="15202-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15202-113">-DefaultProfile</span></span>
<span data-ttu-id="15202-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15202-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15202-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="15202-115">-GroupId</span></span>
<span data-ttu-id="15202-116">Especifica o identificador de um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="15202-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="15202-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15202-117">-PassThru</span></span>
<span data-ttu-id="15202-118">Indica que esse cmdlet retorna um valor de $True se tiver êxito ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="15202-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="15202-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="15202-119">-Confirm</span></span>
<span data-ttu-id="15202-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15202-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15202-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15202-121">-WhatIf</span></span>
<span data-ttu-id="15202-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="15202-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15202-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15202-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15202-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15202-124">CommonParameters</span></span>
<span data-ttu-id="15202-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15202-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15202-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15202-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15202-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15202-127">INPUTS</span></span>

### <span data-ttu-id="15202-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="15202-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="15202-129">System. String</span><span class="sxs-lookup"><span data-stu-id="15202-129">System.String</span></span>

### <span data-ttu-id="15202-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="15202-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="15202-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15202-131">OUTPUTS</span></span>

### <span data-ttu-id="15202-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15202-132">System.Boolean</span></span>

## <span data-ttu-id="15202-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15202-133">NOTES</span></span>

## <span data-ttu-id="15202-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15202-134">RELATED LINKS</span></span>

[<span data-ttu-id="15202-135">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="15202-135">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="15202-136">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="15202-136">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="15202-137">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="15202-137">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


