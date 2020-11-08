---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: f4e2bb2bce0dc01f99b55497ba671999c9c2ab01
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116148"
---
# <span data-ttu-id="2a3fb-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2a3fb-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="2a3fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a3fb-102">SYNOPSIS</span></span>
<span data-ttu-id="2a3fb-103">Configura um grupo de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-103">Configures an API management group.</span></span>

## <span data-ttu-id="2a3fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a3fb-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a3fb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a3fb-105">DESCRIPTION</span></span>
<span data-ttu-id="2a3fb-106">O cmdlet **set-AzApiManagementGroup** configura um grupo de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="2a3fb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a3fb-107">EXAMPLES</span></span>

### <span data-ttu-id="2a3fb-108">Exemplo 1: configurar um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2a3fb-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="2a3fb-109">Esse comando configura um grupo de gerenciamento chamado Group0001.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="2a3fb-110">OS</span><span class="sxs-lookup"><span data-stu-id="2a3fb-110">PARAMETERS</span></span>

### <span data-ttu-id="2a3fb-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2a3fb-111">-Context</span></span>
<span data-ttu-id="2a3fb-112">Especifica uma instância de um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2a3fb-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a3fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a3fb-113">-DefaultProfile</span></span>
<span data-ttu-id="2a3fb-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a3fb-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="2a3fb-115">-Description</span></span>
<span data-ttu-id="2a3fb-116">Especifica a descrição do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-116">Specifies the description of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a3fb-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="2a3fb-117">-GroupId</span></span>
<span data-ttu-id="2a3fb-118">Especifica o identificador do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="2a3fb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a3fb-119">-Name</span></span>
<span data-ttu-id="2a3fb-120">Especifica o nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-120">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a3fb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a3fb-121">-PassThru</span></span>
<span data-ttu-id="2a3fb-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="2a3fb-122">passthru</span></span>

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

### <span data-ttu-id="2a3fb-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2a3fb-123">-Confirm</span></span>
<span data-ttu-id="2a3fb-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a3fb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a3fb-125">-WhatIf</span></span>
<span data-ttu-id="2a3fb-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a3fb-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a3fb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a3fb-128">CommonParameters</span></span>
<span data-ttu-id="2a3fb-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a3fb-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a3fb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a3fb-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a3fb-131">INPUTS</span></span>

### <span data-ttu-id="2a3fb-132">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2a3fb-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2a3fb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2a3fb-133">System.String</span></span>

### <span data-ttu-id="2a3fb-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2a3fb-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a3fb-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a3fb-135">OUTPUTS</span></span>

### <span data-ttu-id="2a3fb-136">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2a3fb-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="2a3fb-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a3fb-137">NOTES</span></span>

## <span data-ttu-id="2a3fb-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a3fb-138">RELATED LINKS</span></span>

[<span data-ttu-id="2a3fb-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2a3fb-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="2a3fb-140">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2a3fb-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="2a3fb-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2a3fb-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


