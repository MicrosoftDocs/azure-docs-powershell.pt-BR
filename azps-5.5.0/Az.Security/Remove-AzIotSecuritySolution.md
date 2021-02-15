---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118710"
---
# <span data-ttu-id="b1583-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="b1583-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="b1583-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1583-102">SYNOPSIS</span></span>
<span data-ttu-id="b1583-103">Excluir solução de segurança de IoT</span><span class="sxs-lookup"><span data-stu-id="b1583-103">Delete IoT security solution</span></span>

## <span data-ttu-id="b1583-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1583-104">SYNTAX</span></span>

### <span data-ttu-id="b1583-105">ResourceGroupLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b1583-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1583-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="b1583-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1583-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="b1583-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1583-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1583-108">DESCRIPTION</span></span>
<span data-ttu-id="b1583-109">O Remove-AzIotSecuritySolution cmdlet exclui uma solução de segurança iot específica.</span><span class="sxs-lookup"><span data-stu-id="b1583-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="b1583-110">A solução de segurança de IoT coleta dados e eventos de segurança de dispositivos iot e hub iot para ajudar a evitar e detectar ameaças.</span><span class="sxs-lookup"><span data-stu-id="b1583-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="b1583-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b1583-111">EXAMPLES</span></span>

### <span data-ttu-id="b1583-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1583-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="b1583-113">Excluir solução de segurança IoT "MySample" com o grupo de recursos "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="b1583-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="b1583-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1583-114">PARAMETERS</span></span>

### <span data-ttu-id="b1583-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1583-115">-DefaultProfile</span></span>
<span data-ttu-id="b1583-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1583-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1583-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1583-117">-InputObject</span></span>
<span data-ttu-id="b1583-118">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="b1583-118">Input Object.</span></span>

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

### <span data-ttu-id="b1583-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1583-119">-Name</span></span>
<span data-ttu-id="b1583-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b1583-120">Resource name.</span></span>

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

### <span data-ttu-id="b1583-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1583-121">-PassThru</span></span>
<span data-ttu-id="b1583-122">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b1583-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="b1583-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1583-123">-ResourceGroupName</span></span>
<span data-ttu-id="b1583-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b1583-124">Resource group name.</span></span>

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

### <span data-ttu-id="b1583-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1583-125">-ResourceId</span></span>
<span data-ttu-id="b1583-126">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="b1583-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="b1583-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b1583-127">-Confirm</span></span>
<span data-ttu-id="b1583-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1583-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1583-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1583-129">-WhatIf</span></span>
<span data-ttu-id="b1583-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b1583-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1583-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1583-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1583-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1583-132">CommonParameters</span></span>
<span data-ttu-id="b1583-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1583-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1583-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1583-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1583-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="b1583-135">INPUTS</span></span>

### <span data-ttu-id="b1583-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b1583-136">System.String</span></span>

### <span data-ttu-id="b1583-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="b1583-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="b1583-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="b1583-138">OUTPUTS</span></span>

### <span data-ttu-id="b1583-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1583-139">System.Boolean</span></span>

## <span data-ttu-id="b1583-140">Notas</span><span class="sxs-lookup"><span data-stu-id="b1583-140">NOTES</span></span>

## <span data-ttu-id="b1583-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1583-141">RELATED LINKS</span></span>
