---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: a2de03f28935fb8002966e0e9251218809ddec5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887795"
---
# <span data-ttu-id="9bf7e-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="9bf7e-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="9bf7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bf7e-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf7e-103">Define uma nova senha para um usuário no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9bf7e-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="9bf7e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9bf7e-104">SYNTAX</span></span>

### <span data-ttu-id="9bf7e-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9bf7e-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bf7e-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bf7e-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bf7e-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bf7e-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bf7e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9bf7e-108">DESCRIPTION</span></span>
<span data-ttu-id="9bf7e-109">O cmdlet **Set-AzDataBoxEdgeUser** define uma nova senha para um usuário no dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="9bf7e-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="9bf7e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9bf7e-110">EXAMPLES</span></span>

### <span data-ttu-id="9bf7e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9bf7e-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="9bf7e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9bf7e-112">PARAMETERS</span></span>

### <span data-ttu-id="9bf7e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bf7e-113">-AsJob</span></span>
<span data-ttu-id="9bf7e-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9bf7e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bf7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf7e-115">-DefaultProfile</span></span>
<span data-ttu-id="9bf7e-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf7e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bf7e-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9bf7e-117">-DeviceName</span></span>
<span data-ttu-id="9bf7e-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="9bf7e-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf7e-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9bf7e-119">-EncryptionKey</span></span>
<span data-ttu-id="9bf7e-120">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="9bf7e-120">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf7e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bf7e-121">-InputObject</span></span>
<span data-ttu-id="9bf7e-122">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="9bf7e-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf7e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9bf7e-123">-Name</span></span>
<span data-ttu-id="9bf7e-124">Username</span><span class="sxs-lookup"><span data-stu-id="9bf7e-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf7e-125">-Password</span><span class="sxs-lookup"><span data-stu-id="9bf7e-125">-Password</span></span>
<span data-ttu-id="9bf7e-126">Senha, forneça como uma cadeia de caracteres segura</span><span class="sxs-lookup"><span data-stu-id="9bf7e-126">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf7e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf7e-127">-ResourceGroupName</span></span>
<span data-ttu-id="9bf7e-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="9bf7e-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf7e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bf7e-129">-ResourceId</span></span>
<span data-ttu-id="9bf7e-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bf7e-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf7e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bf7e-131">-Confirm</span></span>
<span data-ttu-id="9bf7e-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bf7e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bf7e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bf7e-133">-WhatIf</span></span>
<span data-ttu-id="9bf7e-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9bf7e-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bf7e-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9bf7e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bf7e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf7e-136">CommonParameters</span></span>
<span data-ttu-id="9bf7e-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf7e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf7e-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bf7e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf7e-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9bf7e-139">INPUTS</span></span>

### <span data-ttu-id="9bf7e-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9bf7e-140">None</span></span>

## <span data-ttu-id="9bf7e-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9bf7e-141">OUTPUTS</span></span>

### <span data-ttu-id="9bf7e-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="9bf7e-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="9bf7e-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="9bf7e-143">NOTES</span></span>

## <span data-ttu-id="9bf7e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bf7e-144">RELATED LINKS</span></span>
