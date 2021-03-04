---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 1685b9607108fa0b7795fb0ed2c69eb94735fc5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888756"
---
# <span data-ttu-id="16e86-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="16e86-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="16e86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16e86-102">SYNOPSIS</span></span>
<span data-ttu-id="16e86-103">Habilita ou desabilita o acesso do locatário.</span><span class="sxs-lookup"><span data-stu-id="16e86-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="16e86-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="16e86-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16e86-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="16e86-105">DESCRIPTION</span></span>
<span data-ttu-id="16e86-106">O cmdlet **Set-AzApiManagementTenantAccess** habilita ou desabilita o acesso do locatário.</span><span class="sxs-lookup"><span data-stu-id="16e86-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="16e86-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16e86-107">EXAMPLES</span></span>

### <span data-ttu-id="16e86-108">Exemplo 1: Habilitar o acesso de locatários</span><span class="sxs-lookup"><span data-stu-id="16e86-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="16e86-109">Esse comando habilita o acesso do locatário no contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="16e86-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="16e86-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="16e86-110">PARAMETERS</span></span>

### <span data-ttu-id="16e86-111">-Context</span><span class="sxs-lookup"><span data-stu-id="16e86-111">-Context</span></span>
<span data-ttu-id="16e86-112">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="16e86-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="16e86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e86-113">-DefaultProfile</span></span>
<span data-ttu-id="16e86-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="16e86-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16e86-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="16e86-115">-Enabled</span></span>
<span data-ttu-id="16e86-116">Especifica se esse cmdlet habilita ou desabilita o acesso do locatário.</span><span class="sxs-lookup"><span data-stu-id="16e86-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="16e86-117">Especifique um valor de $True para habilitar ou $False desabilitar.</span><span class="sxs-lookup"><span data-stu-id="16e86-117">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e86-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16e86-118">-PassThru</span></span>
<span data-ttu-id="16e86-119">Indica que esse cmdlet retorna **a PsApiManagementAccessInformation** que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="16e86-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="16e86-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e86-120">CommonParameters</span></span>
<span data-ttu-id="16e86-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e86-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e86-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16e86-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e86-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16e86-123">INPUTS</span></span>

### <span data-ttu-id="16e86-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="16e86-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="16e86-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="16e86-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="16e86-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="16e86-126">OUTPUTS</span></span>

### <span data-ttu-id="16e86-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="16e86-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="16e86-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="16e86-128">NOTES</span></span>

## <span data-ttu-id="16e86-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16e86-129">RELATED LINKS</span></span>

[<span data-ttu-id="16e86-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="16e86-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


