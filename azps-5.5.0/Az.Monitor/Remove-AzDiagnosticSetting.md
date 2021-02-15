---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f165396d5b3af823d91e7c06d2f1cb93eb2eaafd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111745"
---
# <span data-ttu-id="54c42-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="54c42-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="54c42-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54c42-102">SYNOPSIS</span></span>
<span data-ttu-id="54c42-103">Remover uma configuração de diagnóstico para o recurso.</span><span class="sxs-lookup"><span data-stu-id="54c42-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="54c42-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54c42-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54c42-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="54c42-105">DESCRIPTION</span></span>
<span data-ttu-id="54c42-106">O cmdlet **Remove-AzDiagnosticSetting** remove a configuração de diagnóstico do recurso específico.</span><span class="sxs-lookup"><span data-stu-id="54c42-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="54c42-107">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="54c42-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="54c42-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="54c42-108">EXAMPLES</span></span>

### <span data-ttu-id="54c42-109">Exemplo 1: Remover a configuração de diagnóstico padrão (serviço) de um recurso</span><span class="sxs-lookup"><span data-stu-id="54c42-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="54c42-110">Esse comando remove a configuração de diagnóstico padrão (serviço) do recurso chamado Resource01.</span><span class="sxs-lookup"><span data-stu-id="54c42-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="54c42-111">Exemplo 2: Remover a configuração de diagnóstico padrão identificada pelo nome determinado de um recurso</span><span class="sxs-lookup"><span data-stu-id="54c42-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="54c42-112">Esse comando remove a configuração de diagnóstico chamada myDiagSetting para o recurso chamado Resource01.</span><span class="sxs-lookup"><span data-stu-id="54c42-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="54c42-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54c42-113">PARAMETERS</span></span>

### <span data-ttu-id="54c42-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c42-114">-DefaultProfile</span></span>
<span data-ttu-id="54c42-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="54c42-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c42-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="54c42-116">-Name</span></span>
<span data-ttu-id="54c42-117">O nome da configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="54c42-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="54c42-118">Se não receber o padrão de chamada como "serviço", como estava na API anterior, esse cmdlet desabilitará apenas todas as categorias para métricas/logs.</span><span class="sxs-lookup"><span data-stu-id="54c42-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="54c42-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54c42-119">-ResourceId</span></span>
<span data-ttu-id="54c42-120">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="54c42-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="54c42-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="54c42-121">-Confirm</span></span>
<span data-ttu-id="54c42-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54c42-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c42-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c42-123">-WhatIf</span></span>
<span data-ttu-id="54c42-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="54c42-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54c42-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="54c42-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c42-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c42-126">CommonParameters</span></span>
<span data-ttu-id="54c42-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c42-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c42-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54c42-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c42-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="54c42-129">INPUTS</span></span>

### <span data-ttu-id="54c42-130">System.String</span><span class="sxs-lookup"><span data-stu-id="54c42-130">System.String</span></span>

## <span data-ttu-id="54c42-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="54c42-131">OUTPUTS</span></span>

### <span data-ttu-id="54c42-132">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="54c42-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="54c42-133">Notas</span><span class="sxs-lookup"><span data-stu-id="54c42-133">NOTES</span></span>

## <span data-ttu-id="54c42-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54c42-134">RELATED LINKS</span></span>

<span data-ttu-id="54c42-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="54c42-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
