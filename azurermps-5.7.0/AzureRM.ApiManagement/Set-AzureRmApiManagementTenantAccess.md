---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 55158ac4f6489d70e17008c9e8c4ef13bd6d4fe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610676"
---
# <span data-ttu-id="736f1-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="736f1-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="736f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="736f1-102">SYNOPSIS</span></span>
<span data-ttu-id="736f1-103">Habilita ou desabilita o acesso do locatário.</span><span class="sxs-lookup"><span data-stu-id="736f1-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="736f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="736f1-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="736f1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="736f1-105">DESCRIPTION</span></span>
<span data-ttu-id="736f1-106">O cmdlet **set-AzureRmApiManagementTenantAccess** habilita ou desabilita o acesso do locatário.</span><span class="sxs-lookup"><span data-stu-id="736f1-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="736f1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="736f1-107">EXAMPLES</span></span>

### <span data-ttu-id="736f1-108">Exemplo 1: habilitar o acesso ao locatário</span><span class="sxs-lookup"><span data-stu-id="736f1-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="736f1-109">Esse comando habilita o acesso do locatário no contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="736f1-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="736f1-110">OS</span><span class="sxs-lookup"><span data-stu-id="736f1-110">PARAMETERS</span></span>

### <span data-ttu-id="736f1-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="736f1-111">-Context</span></span>
<span data-ttu-id="736f1-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="736f1-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="736f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="736f1-113">-DefaultProfile</span></span>
<span data-ttu-id="736f1-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="736f1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="736f1-115">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="736f1-115">-Enabled</span></span>
<span data-ttu-id="736f1-116">Especifica se esse cmdlet habilita ou desabilita o acesso ao locatário.</span><span class="sxs-lookup"><span data-stu-id="736f1-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="736f1-117">Especifique um valor de $True para habilitar ou $False para desabilitar.</span><span class="sxs-lookup"><span data-stu-id="736f1-117">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="736f1-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="736f1-118">-PassThru</span></span>
<span data-ttu-id="736f1-119">Indica que esse cmdlet retorna o **PsApiManagementAccessInformation** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="736f1-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="736f1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="736f1-120">CommonParameters</span></span>
<span data-ttu-id="736f1-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="736f1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="736f1-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="736f1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="736f1-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="736f1-123">INPUTS</span></span>

### <span data-ttu-id="736f1-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="736f1-124">None</span></span>
<span data-ttu-id="736f1-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="736f1-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="736f1-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="736f1-126">OUTPUTS</span></span>

### <span data-ttu-id="736f1-127">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="736f1-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="736f1-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="736f1-128">NOTES</span></span>

## <span data-ttu-id="736f1-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="736f1-129">RELATED LINKS</span></span>

[<span data-ttu-id="736f1-130">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="736f1-130">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


