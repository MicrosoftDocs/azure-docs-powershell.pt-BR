---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113975"
---
# <span data-ttu-id="58597-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="58597-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="58597-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58597-102">SYNOPSIS</span></span>
<span data-ttu-id="58597-103">Excluir a solução de segurança IoT</span><span class="sxs-lookup"><span data-stu-id="58597-103">Delete IoT security solution</span></span>

## <span data-ttu-id="58597-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58597-104">SYNTAX</span></span>

### <span data-ttu-id="58597-105">ResourceGroupLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="58597-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58597-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="58597-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58597-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="58597-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58597-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58597-108">DESCRIPTION</span></span>
<span data-ttu-id="58597-109">O cmdlet Remove-AzIotSecuritySolution exclui uma solução de segurança IOT específica.</span><span class="sxs-lookup"><span data-stu-id="58597-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="58597-110">A solução de segurança da IoT coleta dados de segurança e eventos de dispositivos IOT e Hub IOT para ajudar a prevenir e a detectar ameaças.</span><span class="sxs-lookup"><span data-stu-id="58597-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="58597-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58597-111">EXAMPLES</span></span>

### <span data-ttu-id="58597-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="58597-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="58597-113">Excluir a solução de segurança IoT "MySample" com grupo de recursos "MyResource Group"</span><span class="sxs-lookup"><span data-stu-id="58597-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="58597-114">OS</span><span class="sxs-lookup"><span data-stu-id="58597-114">PARAMETERS</span></span>

### <span data-ttu-id="58597-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58597-115">-DefaultProfile</span></span>
<span data-ttu-id="58597-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58597-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58597-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58597-117">-InputObject</span></span>
<span data-ttu-id="58597-118">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="58597-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58597-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="58597-119">-Name</span></span>
<span data-ttu-id="58597-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="58597-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58597-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58597-121">-PassThru</span></span>
<span data-ttu-id="58597-122">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="58597-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="58597-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58597-123">-ResourceGroupName</span></span>
<span data-ttu-id="58597-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="58597-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58597-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58597-125">-ResourceId</span></span>
<span data-ttu-id="58597-126">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="58597-126">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58597-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="58597-127">-Confirm</span></span>
<span data-ttu-id="58597-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58597-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58597-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58597-129">-WhatIf</span></span>
<span data-ttu-id="58597-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58597-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58597-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58597-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58597-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58597-132">CommonParameters</span></span>
<span data-ttu-id="58597-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58597-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58597-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58597-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58597-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58597-135">INPUTS</span></span>

### <span data-ttu-id="58597-136">System. String</span><span class="sxs-lookup"><span data-stu-id="58597-136">System.String</span></span>

### <span data-ttu-id="58597-137">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="58597-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="58597-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58597-138">OUTPUTS</span></span>

### <span data-ttu-id="58597-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58597-139">System.Boolean</span></span>

## <span data-ttu-id="58597-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58597-140">NOTES</span></span>

## <span data-ttu-id="58597-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58597-141">RELATED LINKS</span></span>
