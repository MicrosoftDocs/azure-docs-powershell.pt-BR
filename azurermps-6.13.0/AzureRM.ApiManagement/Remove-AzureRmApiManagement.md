---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: cee512445f457e7353d5766cd561788b00360b40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609865"
---
# <span data-ttu-id="5a675-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a675-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="5a675-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a675-102">SYNOPSIS</span></span>
<span data-ttu-id="5a675-103">Remove um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="5a675-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a675-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a675-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a675-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a675-105">DESCRIPTION</span></span>
<span data-ttu-id="5a675-106">O cmdlet **Remove-AzureRmApiManagement** remove um serviço de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="5a675-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="5a675-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a675-107">EXAMPLES</span></span>

### <span data-ttu-id="5a675-108">Exemplo 1: remover um serviço de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="5a675-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="5a675-109">Esse comando Remove o serviço de gerenciamento de API chamado ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="5a675-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="5a675-110">OS</span><span class="sxs-lookup"><span data-stu-id="5a675-110">PARAMETERS</span></span>

### <span data-ttu-id="5a675-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a675-111">-DefaultProfile</span></span>
<span data-ttu-id="5a675-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a675-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a675-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a675-113">-Name</span></span>
<span data-ttu-id="5a675-114">Especifica o nome da implantação de gerenciamento de API que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="5a675-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5a675-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a675-115">-PassThru</span></span>
<span data-ttu-id="5a675-116">Indica que esse cmdlet retorna um valor de $True se a operação for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5a675-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="5a675-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a675-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a675-118">Especifica o nome do grupo de recursos sob o qual existe a implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="5a675-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="5a675-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5a675-119">-Confirm</span></span>
<span data-ttu-id="5a675-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a675-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a675-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a675-121">-WhatIf</span></span>
<span data-ttu-id="5a675-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5a675-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a675-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a675-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a675-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a675-124">CommonParameters</span></span>
<span data-ttu-id="5a675-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a675-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a675-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a675-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a675-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a675-127">INPUTS</span></span>

### <span data-ttu-id="5a675-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5a675-128">System.String</span></span>

## <span data-ttu-id="5a675-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a675-129">OUTPUTS</span></span>

### <span data-ttu-id="5a675-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a675-130">System.Boolean</span></span>

## <span data-ttu-id="5a675-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a675-131">NOTES</span></span>

## <span data-ttu-id="5a675-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a675-132">RELATED LINKS</span></span>

[<span data-ttu-id="5a675-133">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a675-133">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="5a675-134">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a675-134">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="5a675-135">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a675-135">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="5a675-136">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a675-136">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


