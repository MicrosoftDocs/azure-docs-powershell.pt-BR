---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 2f62b33b7a5a2224f54be765d03f72fc1667cec1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440419"
---
# <span data-ttu-id="e7228-101">Remove-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="e7228-101">Remove-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="e7228-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7228-102">SYNOPSIS</span></span>
<span data-ttu-id="e7228-103">Remover uma configuração de diagnóstico do recurso a.</span><span class="sxs-lookup"><span data-stu-id="e7228-103">Remove a diagnostic setting for the a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7228-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7228-104">SYNTAX</span></span>

```
Remove-AzureRmDiagnosticSetting -ResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7228-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7228-105">DESCRIPTION</span></span>
<span data-ttu-id="e7228-106">O cmdlet **Remove-AzureRmDiagnosticSetting** remove a configuração de diagnóstico do recurso específico.</span><span class="sxs-lookup"><span data-stu-id="e7228-106">The **Remove-AzureRmDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="e7228-107">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="e7228-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e7228-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7228-108">EXAMPLES</span></span>

### <span data-ttu-id="e7228-109">Exemplo 1: remover a configuração de diagnóstico padrão (serviço) de um recurso</span><span class="sxs-lookup"><span data-stu-id="e7228-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzureRmDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="e7228-110">Esse comando Remove a configuração de diagnóstico padrão (serviço) do recurso chamado Resource01.</span><span class="sxs-lookup"><span data-stu-id="e7228-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="e7228-111">Exemplo 2: remover a configuração de diagnóstico padrão identificada pelo nome fornecido para um recurso</span><span class="sxs-lookup"><span data-stu-id="e7228-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzureRmDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="e7228-112">Esse comando Remove a configuração de diagnóstico chamada myDiagSetting para o recurso chamado Resource01.</span><span class="sxs-lookup"><span data-stu-id="e7228-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="e7228-113">OS</span><span class="sxs-lookup"><span data-stu-id="e7228-113">PARAMETERS</span></span>

### <span data-ttu-id="e7228-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7228-114">-DefaultProfile</span></span>
<span data-ttu-id="e7228-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7228-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7228-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7228-116">-Name</span></span>
<span data-ttu-id="e7228-117">O nome da configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="e7228-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="e7228-118">Se não receber a chamada como padrão para "serviço" como estava na API anterior e esse cmdlet desabilitará apenas todas as categorias de métricas/logs.</span><span class="sxs-lookup"><span data-stu-id="e7228-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="e7228-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7228-119">-ResourceId</span></span>
<span data-ttu-id="e7228-120">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e7228-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="e7228-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7228-121">-Confirm</span></span>
<span data-ttu-id="e7228-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7228-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7228-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7228-123">-WhatIf</span></span>
<span data-ttu-id="e7228-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7228-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7228-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7228-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7228-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7228-126">CommonParameters</span></span>
<span data-ttu-id="e7228-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7228-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7228-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7228-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7228-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7228-129">INPUTS</span></span>

### <span data-ttu-id="e7228-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e7228-130">System.String</span></span>

## <span data-ttu-id="e7228-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7228-131">OUTPUTS</span></span>

### <span data-ttu-id="e7228-132">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e7228-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e7228-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7228-133">NOTES</span></span>

## <span data-ttu-id="e7228-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7228-134">RELATED LINKS</span></span>

<span data-ttu-id="e7228-135">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md) 
 [Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="e7228-135">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)
[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)</span></span>
