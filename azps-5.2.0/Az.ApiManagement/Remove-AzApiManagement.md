---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: f54998dc0d5ec8570a573870148a8cf05c265618
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259196"
---
# <span data-ttu-id="374ef-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="374ef-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="374ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="374ef-102">SYNOPSIS</span></span>
<span data-ttu-id="374ef-103">Remove um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="374ef-103">Removes an API Management service.</span></span>

## <span data-ttu-id="374ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="374ef-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="374ef-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="374ef-105">DESCRIPTION</span></span>
<span data-ttu-id="374ef-106">O cmdlet **Remove-AzApiManagement** remove um serviço de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="374ef-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="374ef-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="374ef-107">EXAMPLES</span></span>

### <span data-ttu-id="374ef-108">Exemplo 1: remover um serviço de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="374ef-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="374ef-109">Esse comando Remove o serviço de gerenciamento de API chamado ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="374ef-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="374ef-110">OS</span><span class="sxs-lookup"><span data-stu-id="374ef-110">PARAMETERS</span></span>

### <span data-ttu-id="374ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="374ef-111">-DefaultProfile</span></span>
<span data-ttu-id="374ef-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="374ef-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="374ef-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="374ef-113">-Name</span></span>
<span data-ttu-id="374ef-114">Especifica o nome da implantação de gerenciamento de API que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="374ef-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="374ef-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="374ef-115">-PassThru</span></span>
<span data-ttu-id="374ef-116">Indica que esse cmdlet retorna um valor de $True se a operação for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="374ef-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="374ef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="374ef-117">-ResourceGroupName</span></span>
<span data-ttu-id="374ef-118">Especifica o nome do grupo de recursos sob o qual existe a implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="374ef-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="374ef-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="374ef-119">-Confirm</span></span>
<span data-ttu-id="374ef-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="374ef-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="374ef-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="374ef-121">-WhatIf</span></span>
<span data-ttu-id="374ef-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="374ef-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="374ef-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="374ef-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="374ef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="374ef-124">CommonParameters</span></span>
<span data-ttu-id="374ef-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="374ef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="374ef-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="374ef-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="374ef-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="374ef-127">INPUTS</span></span>

### <span data-ttu-id="374ef-128">System. String</span><span class="sxs-lookup"><span data-stu-id="374ef-128">System.String</span></span>

## <span data-ttu-id="374ef-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="374ef-129">OUTPUTS</span></span>

### <span data-ttu-id="374ef-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="374ef-130">System.Boolean</span></span>

## <span data-ttu-id="374ef-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="374ef-131">NOTES</span></span>

## <span data-ttu-id="374ef-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="374ef-132">RELATED LINKS</span></span>

[<span data-ttu-id="374ef-133">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="374ef-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="374ef-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="374ef-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="374ef-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="374ef-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="374ef-136">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="374ef-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


