---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110885"
---
# <span data-ttu-id="913f7-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="913f7-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="913f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="913f7-102">SYNOPSIS</span></span>
<span data-ttu-id="913f7-103">Define uma nova senha para um usuário no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="913f7-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="913f7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="913f7-104">SYNTAX</span></span>

### <span data-ttu-id="913f7-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="913f7-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="913f7-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="913f7-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="913f7-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="913f7-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="913f7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="913f7-108">DESCRIPTION</span></span>
<span data-ttu-id="913f7-109">O cmdlet **Set-AzSt stackEdgeUser** define uma nova senha para um usuário no dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="913f7-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="913f7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="913f7-110">EXAMPLES</span></span>

### <span data-ttu-id="913f7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="913f7-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="913f7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="913f7-112">PARAMETERS</span></span>

### <span data-ttu-id="913f7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="913f7-113">-AsJob</span></span>
<span data-ttu-id="913f7-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="913f7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="913f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913f7-115">-DefaultProfile</span></span>
<span data-ttu-id="913f7-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="913f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="913f7-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="913f7-117">-DeviceName</span></span>
<span data-ttu-id="913f7-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="913f7-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913f7-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="913f7-119">-EncryptionKey</span></span>
<span data-ttu-id="913f7-120">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="913f7-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="913f7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="913f7-121">-InputObject</span></span>
<span data-ttu-id="913f7-122">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="913f7-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases: User

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913f7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="913f7-123">-Name</span></span>
<span data-ttu-id="913f7-124">Username</span><span class="sxs-lookup"><span data-stu-id="913f7-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913f7-125">-Senha</span><span class="sxs-lookup"><span data-stu-id="913f7-125">-Password</span></span>
<span data-ttu-id="913f7-126">Senha, fornecer como uma cadeia de caracteres segura</span><span class="sxs-lookup"><span data-stu-id="913f7-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="913f7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="913f7-127">-ResourceGroupName</span></span>
<span data-ttu-id="913f7-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="913f7-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913f7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="913f7-129">-ResourceId</span></span>
<span data-ttu-id="913f7-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="913f7-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913f7-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="913f7-131">-Confirm</span></span>
<span data-ttu-id="913f7-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="913f7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="913f7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="913f7-133">-WhatIf</span></span>
<span data-ttu-id="913f7-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="913f7-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="913f7-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="913f7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="913f7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913f7-136">CommonParameters</span></span>
<span data-ttu-id="913f7-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="913f7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913f7-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="913f7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913f7-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="913f7-139">INPUTS</span></span>

### <span data-ttu-id="913f7-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="913f7-140">None</span></span>

## <span data-ttu-id="913f7-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="913f7-141">OUTPUTS</span></span>

### <span data-ttu-id="913f7-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="913f7-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="913f7-143">Notas</span><span class="sxs-lookup"><span data-stu-id="913f7-143">NOTES</span></span>

## <span data-ttu-id="913f7-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="913f7-144">RELATED LINKS</span></span>
