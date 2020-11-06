---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f99a7cfb18b585e1187cac62eb586bac37dad55d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600795"
---
# <span data-ttu-id="9ab8f-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="9ab8f-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="9ab8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ab8f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab8f-103">Remover uma configuração de diagnóstico do recurso a.</span><span class="sxs-lookup"><span data-stu-id="9ab8f-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="9ab8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ab8f-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ab8f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ab8f-105">DESCRIPTION</span></span>
<span data-ttu-id="9ab8f-106">O cmdlet **Remove-AzDiagnosticSetting** remove a configuração de diagnóstico do recurso específico.</span><span class="sxs-lookup"><span data-stu-id="9ab8f-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="9ab8f-107">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="9ab8f-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="9ab8f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ab8f-108">EXAMPLES</span></span>

### <span data-ttu-id="9ab8f-109">Exemplo 1: remover a configuração de diagnóstico padrão (serviço) de um recurso</span><span class="sxs-lookup"><span data-stu-id="9ab8f-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="9ab8f-110">Esse comando Remove a configuração de diagnóstico padrão (serviço) do recurso chamado Resource01.</span><span class="sxs-lookup"><span data-stu-id="9ab8f-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="9ab8f-111">Exemplo 2: remover a configuração de diagnóstico padrão identificada pelo nome fornecido para um recurso</span><span class="sxs-lookup"><span data-stu-id="9ab8f-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="9ab8f-112">Esse comando Remove a configuração de diagnóstico chamada myDiagSetting para o recurso chamado Resource01.</span><span class="sxs-lookup"><span data-stu-id="9ab8f-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="9ab8f-113">OS</span><span class="sxs-lookup"><span data-stu-id="9ab8f-113">PARAMETERS</span></span>

### <span data-ttu-id="9ab8f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ab8f-114">-DefaultProfile</span></span>
<span data-ttu-id="9ab8f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ab8f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ab8f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ab8f-116">-Name</span></span>
<span data-ttu-id="9ab8f-117">O nome da configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="9ab8f-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="9ab8f-118">Se não receber a chamada como padrão para "serviço" como estava na API anterior e esse cmdlet desabilitará apenas todas as categorias de métricas/logs.</span><span class="sxs-lookup"><span data-stu-id="9ab8f-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="9ab8f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ab8f-119">-ResourceId</span></span>
<span data-ttu-id="9ab8f-120">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9ab8f-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="9ab8f-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9ab8f-121">-Confirm</span></span>
<span data-ttu-id="9ab8f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ab8f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ab8f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ab8f-123">-WhatIf</span></span>
<span data-ttu-id="9ab8f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9ab8f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ab8f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9ab8f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ab8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab8f-126">CommonParameters</span></span>
<span data-ttu-id="9ab8f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ab8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab8f-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ab8f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab8f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ab8f-129">INPUTS</span></span>

### <span data-ttu-id="9ab8f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9ab8f-130">System.String</span></span>

## <span data-ttu-id="9ab8f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ab8f-131">OUTPUTS</span></span>

### <span data-ttu-id="9ab8f-132">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9ab8f-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="9ab8f-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ab8f-133">NOTES</span></span>

## <span data-ttu-id="9ab8f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ab8f-134">RELATED LINKS</span></span>

<span data-ttu-id="9ab8f-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="9ab8f-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
