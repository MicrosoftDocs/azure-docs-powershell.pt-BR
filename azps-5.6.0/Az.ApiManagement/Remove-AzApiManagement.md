---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: daa4169ed077003d2ceb773e2e085e72fb6d1ec8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886280"
---
# <span data-ttu-id="34285-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="34285-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="34285-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34285-102">SYNOPSIS</span></span>
<span data-ttu-id="34285-103">Remove um serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="34285-103">Removes an API Management service.</span></span>

## <span data-ttu-id="34285-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="34285-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34285-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="34285-105">DESCRIPTION</span></span>
<span data-ttu-id="34285-106">O cmdlet **Remove-AzApiManagement** remove um serviço de Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="34285-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="34285-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34285-107">EXAMPLES</span></span>

### <span data-ttu-id="34285-108">Exemplo 1: Remover um serviço de Gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="34285-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="34285-109">Este comando remove o serviço de Gerenciamento de API chamado ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="34285-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="34285-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="34285-110">PARAMETERS</span></span>

### <span data-ttu-id="34285-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34285-111">-DefaultProfile</span></span>
<span data-ttu-id="34285-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="34285-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34285-113">-Name</span><span class="sxs-lookup"><span data-stu-id="34285-113">-Name</span></span>
<span data-ttu-id="34285-114">Especifica o nome da implantação de Gerenciamento de API que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="34285-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="34285-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34285-115">-PassThru</span></span>
<span data-ttu-id="34285-116">Indica que esse cmdlet retornará um valor de $True se a operação for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="34285-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="34285-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34285-117">-ResourceGroupName</span></span>
<span data-ttu-id="34285-118">Especifica o nome do grupo de recursos no qual existe a implantação de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="34285-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="34285-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34285-119">-Confirm</span></span>
<span data-ttu-id="34285-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34285-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34285-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34285-121">-WhatIf</span></span>
<span data-ttu-id="34285-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="34285-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34285-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34285-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34285-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34285-124">CommonParameters</span></span>
<span data-ttu-id="34285-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34285-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34285-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34285-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34285-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34285-127">INPUTS</span></span>

### <span data-ttu-id="34285-128">System.String</span><span class="sxs-lookup"><span data-stu-id="34285-128">System.String</span></span>

## <span data-ttu-id="34285-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="34285-129">OUTPUTS</span></span>

### <span data-ttu-id="34285-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="34285-130">System.Boolean</span></span>

## <span data-ttu-id="34285-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="34285-131">NOTES</span></span>

## <span data-ttu-id="34285-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34285-132">RELATED LINKS</span></span>

[<span data-ttu-id="34285-133">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="34285-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="34285-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="34285-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="34285-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="34285-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="34285-136">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="34285-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


